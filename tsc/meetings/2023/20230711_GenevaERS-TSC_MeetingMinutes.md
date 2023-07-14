# Meeting notes TSC 2023-07-11 6pm Pacific Time (US)
All interested in GenevaERS development are welcome to join.
## Conference call details
### Zoom Meeting
https://zoom-lfx.platform.linuxfoundation.org/meeting/95522057563?password=a2cb4656-98bd-4f6e-9d48-2998457acf72
## Administration
- Ask Bob about Nokogiri 
- Review Andrea's draft slide deck for the annual OMP review.
- What do we want to accomplish before our annual OMP review in August? 
  - Publish repos in public GitHub
    - Workbench
    - Test-Framework
      - Split out from the current Java repo 
    - Run-Control-Utilities
    - Performance-Engine 
    - Performance-Engine-R-and-D
    - DevOps (PE build process)
  - Anything else?  
## Workbench
## Performance Engine
- RTC 22485: Research using a hashing algorithm rather than a binary search tree
  - Until now, all of our in-memory reference file searches have used a binary search tree that is built at MR95 initialization time. 
  - We are now introducing a search using a hashing algorithm, which has been shown to reduce the CPU time required in many circumstances. 
  - We will continue to use the binary search tree technique for lookups that require effective dates.  
  - Should all other searches use the hashing technique? 
    - If not, why not? 
    - Do the following factors impact our decision? 
      - The size of the key.
        - **Will make a difference.**
      - The size of the record. 
        - **Will not make a difference.**
      - The number of records.  
        - **Will make a difference.**
    - Should we consider other search algorithms? 
      - For very small tables, a sequential search might be the most efficient. 
  - Should the choice of algorithm be specified in the Workbench or in the JCL?  
    - If in the JCL, should it be for the whole run or for each table?  
      - A table is specified by the combination of LR and LF  
        - **Should make the choice at the table level.**
      - How do we specify this? 
        - Have the MR95 parameters (EXTRPARM) list all the reference files? 
  - If we use the hashing technique, the source records don't need to be sorted. 
    - Definite advantage in some cases. 
  - **Have a default setting**
  - **Modify MR95 parameter file to accept overrides** 
  - **Add statistics**
## Potential users (who may want support)
- Neil's read exit for Adabas is now working.  
  - Opens up market for Adabas users 
    - State governments, US government, large corporations 
## Demo
## Run-Control Utilities 
## Documentation
- "A document a week, that's all we ask" 
## Infrastructure
## R&D Work
## Conferences 
- Possible presentation at the Winter SHARE conference 
## For next time 
### Performance Engine
