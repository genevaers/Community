# Meeting notes TSC 2023-11-28 6pm Pacific Time (US)
All interested in GenevaERS development are welcome to join.
## Conference call details
### Zoom Meeting
https://zoom-lfx.platform.linuxfoundation.org/meeting/95522057563?password=a2cb4656-98bd-4f6e-9d48-2998457acf72
## Attendees 
<!-- - Andrea Orth -->
<!-- - Bob McCormack -->   
<!-- - Eugene Morrow -->
- Gillian Hannington
- Ian Cunningham
- Jeff Horner 
<!-- - Kip Twitchell -->
- Michael Shapiro
- Neil Beesley 
- Randall Ness
## Administration
### TAC 10/12/23
- We need to get move from a passing badge to gold. An issue or project item will be opened on this. Criteria listing for all [OpenSSF badges](https://www.bestpractices.dev/en/criteria)
  - How should we proceed here?   
    - We could create Projects in GitHub.
    - We could create Discussions in GitHub.
      - Randall has posted his proposals for the V5 Format Phase as an "idea" on the GenevaERS discussions page
        - Note: Discussions aren't cloned to your local copy.    
        - Kip: Could you do the same for:
          - the MR95 looping proposal?  
          - the diagram of design options for integrating Java into our technology? 
## Infrastructure
## Run-Control Apps
## Workbench
## R&D Work
- Sort utilities for UNIX 
- Byte Buddy 
- Liberty - open source alternative to WebSphere.
## Performance Engine
- Aggregation functions
  - **Gill will create an idea document.**
- MR95 parameters to support table lookups using a hashing algorithm  
- Java bytecode 
  - What is the minimum possible bytecode program we could develop?
    - "HELLO WORLD"
## Potential users (who may want support)
## Demo
## Documentation
- Technical documentation 
- "A document a week, that's all we ask" 
## Conferences 
- Possible presentation at the Winter SHARE conference 
## For next time 
- Randall will compare MR95 to CICS. 
# Proposals for enhancements to the lookup process 
## Performance considerations
- The best lookup is no lookup 
  - Avoid doing lookups whenever possible 
- Having fewer instructions is better
  - Do as much in initialization as possible to minimize the instruction path during the main loop 
- Keeping data and instructions in cache is really important
  - Also should avoid crossing cache line boundaries
- Long jumps are expensive 
  - The next instructions need to be copied into L1 cache, and the longer the jump is, the more likely it is that the processor would have to get the next instructions from L2, L3, or even main memory 
- Branches should be avoided if possible
  - The size of the branch prediction buffer is limited and shouldn’t be wasted
- Compare instructions are expensive 
  - The processor tries to predict where the next instruction is, but it’s not perfect
  - Reduce the number of comparisons if possible
- EXECUTE instructions (EX, EXRL) are expensive 
  - They are like one-line subroutines which disrupt the logical flow of instructions and hurt pipelining 
## Background information on lookups
- There are two logic table functions for lookups:
  - LUSM (Look Up to a Structure in Memory) - internal table
  - LUEX (Look Up using an Exit)
    - This is like a function call
      - The lookup key is like the parameters passed to a function
      - The lookup data is like the results passed back from a function   
    - Someday we may extend GenevaERS to use logic text for the lookup logic instead of a called program 
    - Traditionally, these have been the most common lookups 
- There are two kinds of lookup optimization:
  - Avoiding lookups for the same record 
    - Using the same record implies that you are using the same key, but it’s a simpler check than checking for the same key
      - That would require building the key first
  - Avoiding lookups for the same key as the last lookup 
    - The last lookup may have been on the immediately prior record or several records before if records were filtered out
    - In the current MR95, this check is not being done for LUSM lookups which resulted in a not-found on the prior lookup 
      - But it should be 
    - Also, in the current MR95, this check is not being done for any LUEX lookups at all 
      - But it should be 
    - For effective-dated lookups, we will have to check the dates as well as the key value 
    - The current MR95 has the key-check logic in the SRCHTBL paragraph
      - This should be moved out to the model code
        - This will reduce the number of instructions and avoid an EX instruction 
- Optimization can be applied to any LUSM 
- Optimization can be applied to an LUEX only if the Optimize box has been checked for the User-Exit in the Workbench 
- Last-key optimization can be applied only to the first step of a multi-step lookup
  - Subsequent steps normally depend on the results of the first step, so there is no good way to optimize them 
- A lookup is considered unconditional if it is always executed in an ES set (source logical file) 
  - All other lookups are considered conditional
- A lookup may be executed before the views in a logic table only if it is both unconditional and optimizable
- For reporting purposes, we shouldn’t be counting lookups which have been optimized away 
  - The current MR95 is inconsistent about this 
    - It counts lookups which have been optimized away by virtue of having the same key, but not those which are on the same record 
- Each unique lookup type is assigned a Runtime Lookup Path ID by MR91
  - A given lookup path defined with symbolics will be assigned a separate Runtime Lookup Path ID for each unique combination of symbolics assigned in the logic text 
    - The same is true for effective-dated lookups with different Effective Date Types
- MR95 creates a separate lookup buffer for each Runtime Lookup Path ID (and step?)  
## Proposals 
- Move key-build and lookup rows to a lookup subroutine (or “EL set”) 
  - Replace key-build/lookup sequences with a CLLU (Call Lookup Subroutine) row 
  - Insert a CKRN (Check Record Number) row before each optimizable CLLU row except the first for each unique lookup type (Runtime Lookup Path ID)
    - There is no need to check the record number at that point 
  - This modification will lead to the greatest compression of the logic table and generated code, which should improve cache performance
- Create model code for our current SRCHTBL routine and customize the generated code for each runtime lookup path
  - Use a Compare instruction with the actual key length rather than an Execute instruction
    - Avoiding the use of an Execute instruction will allow the use of a compare-and-branch instruction 
    - [This has been done in PM 4.18]
  - Vary the code based on the use of effective dates 
    - Lookup with no effective dates
    - Lookup with start date only 
    - Lookup with end date only 
    - Lookup with start and end date 
  - Each unique lookup type will point to its proper version 
    - This will reduce the instruction path length
  - Generating specific versions of SRCHTBL will increase the size of the generated code, but this may be compensated for by the lack of EX instructions 
- Clean up the key-check code 
  - Move the key-check code out of the SRCHTBL paragraph and into model code 
    - Logic table function code CKKY (Check Key)
  - Execute CKKY for both found and not-found prior lookups and for both in-memory and optimizable exit lookups
    - This would require checking the effective date or timestamp in certain cases.  
  - Place a CKKY row only after the key-build rows for the first level of a lookup 
- Create dummy lookup result records 
  - During thread initialization, create dummy lookup result records to pre-populate values for not-found lookups and minimize branching
  - In the Initialization section of the logic table, define the dummy record with sequences of LIC (Lookup Initialization from a Constant) rows 
  - Replace DTL-GOTO-DTC combinations with a single DTL
  - Do the same for ADDL, SUBL, MULL, DIVL, CTL, FNEL, FNLL, LKDL, LKL, SETL, SKL 
- Move all LKC and LKS rows from key-build sequences to the thread initialization section
  - There is no need to set constants in the key for every event record
- If a lookup is both unconditional and optimizable, move its rows from the lookup subroutine to the beginning of the ES set, immediately after the RENX or REEX row
  - Remove the associated CKRN and CLLU rows
## Current logic table structure 
```
HD

  [Zero or more ET (token) sets]
    RETK
      …
    ET

  [One or more ES (source logical file) sets]
    RENX
      NV
      DTE
      DTE
      JOIN
      LKE
      LKE
      LUSM
      DTL
      GOTO
      DTC
      WRDT 
      …
    ES

EN
```
## Proposed logic table structure
```
HD

  [Zero or more EI (initialization) sets]
    STIT
      LIC
      LIC
      …
      LKC
      LKC
      …
    EI
    STIT
      LIC
      LIC
      …
      LKC
      LKC
      …
    EI

  [Zero or more EL (lookup) sets]
    STLU
      LKLR
      LKE
      LKE
      CKKY (check key on first level only) 
      LUSM
      LKLR
      LKE
      LKL
      LUSM
    EL
    …
    STLU
      LKLR
      LKE
      LKE
      CKKY 
      LUEX (optimizable) 
    EL
    …
    STLU
      LKLR
      LKE
      LKE
      LUEX (not optimizable) 
    EL 

    [Zero or more ET (token) sets]
      RETK
        …
      ET

    [One or more ES (source logical file) sets]
    RENX
      STLU
        LKLR
        LKE
        LKE
        LUEX (unconditional and optimizable lookup) 
      EL
      …
      NV
        DTE
        CLLU
        DTL
        WRDT
      NV
        DTE
        CKRN
        CLLU
        DTL
        WRDT
      NV
      …
    ES
EN

