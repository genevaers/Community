# Meeting notes TSC 2023-11-21 6pm Pacific Time (US)
All interested in GenevaERS development are welcome to join.
## Conference call details
### Zoom Meeting
https://zoom-lfx.platform.linuxfoundation.org/meeting/95522057563?password=a2cb4656-98bd-4f6e-9d48-2998457acf72
## Attendees 
- Andrea Orth
<!-- - Bob McCormack -->   
<!-- - Eugene Morrow -->
- Gillian Hannington
- Ian Cunningham
<!-- - Jeff Horner --> 
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
- Randall's proposed workplan: 
  - GenevaERS V4.20.001
    - PM 4.18.108
    - WE 4.20.0 OS4
      - We want to finish this ASAP to decouple our product from the C++ code in WE 4.17.  
      - This will also allow us to drop the BIRT (Business Intelligence Reporting Tool) reports.  
  - GenevaERS V4.20.002
    - PM 4.18.109
      - with Java MR91 and Analyzer 
      - We want to finish this ASAP to decouple our product from the C++ in the Run-Control Generator and the Run-Control Analyzer.  
    - WE 4.20.0 OS4
  - GenevaERS V4.21.003
    - PM 4.18.109
    - WE 4.21
      - with MR91 and Analyzer features built-in
        - generate VDPs
        - generate flow pictures 
        - generate VDP spreadsheet for analysis
        - generate logic text reports 
  - GenevaERS V5.01.001
    - PM 5.01.001
      - Long-string support 
        - **Gill will add an issue for this.**
      - Hash-table lookups 
        - **Gill will add an issue for this.**
    - WE 5.01.001
      - Long-string support 
        - **Ian will add an issue for this.**
  - GenevaERS V5.02.001
    - PM 5.02.001
      - Hardcopy feature removed
        - **Gill will add an issue for this.**
    - WE 5.02.001
      - Hardcopy feature removed
        - **Ian will add an issue for this.**
  - Suggestion: Even though it might make sense to branch the Workbench code after WE 4.21, we could make a complete V5 package if we branched the Workbench code after WE 4.20 OS4.  
### Misc
- Before end of year, review the committers .csv and open issues in Community
  - **Done.**
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
