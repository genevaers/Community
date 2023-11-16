# Meeting notes TSC 2023-11-14 6pm Pacific Time (US)
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
- Kip Twitchell 
- Michael Shapiro
- Neil Beesley 
- Randall Ness
## Administration
### TAC 10/12/23
- We need to get move from a passing badge to gold. An issue or project item will be opened on this. Criteria listing for all [OpenSSF badges](https://www.bestpractices.dev/en/criteria)
  - How should we proceed here?   
    - We could create Projects in GitHub.
    - We could create Discussions in GitHub.  
### Misc
- Before end of year, review the committers .csv and open issues in Community
## Infrastructure
## Run-Control Apps
## Workbench
## R&D Work
- Looping in MR95 
- Sort utilities for UNIX 
- Byte Buddy 
- Liberty - open source alternative to WebSphere.
## Performance Engine
- Randall's proposals for the Format Phase in GenevaERS V5
  - Short term 
    - Simplify the current MR88.
      - Remove hardcopy reports.
      - Remove multi-level aggregation.
      - Focus on .csv output.
    - Why? 
      - Any new customers would not likely require hardcopy reports.
      - We want MR88 to be more maintainable. 
    - What other changes would be required? 
      - We'd have to remove the hardcopy features from the Workbench in V5.
  - Long term
    - Option 1
      - Rewrite in Java.
    - Option 2
      - Use MR95 instead of MR88 for the Format Phase 
        - There is precedent.
          - We've already replaced a custom program in the Reference Phase with another execution of MR95.  
            - We created a Join Logic Table (JLT) to support this.
          - We could have MR91 create views that run only in the Format Phase and turn them into a Format Logic Table (FLT), using Extract Work Files as input instead of our traditional data sources.  
        - Just as the Extract Phase supports: 
          - Moves
          - Lookups 
          - Calculations
          - Filtering at the record level 
          - Logic at the column level
        - ...we could do the same to already-summarized records in the Format Phase. 
      - This would allow us to focus on one super-powerful program, MR95, that has the best code for: 
        - I/O
        - Moves
        - Lookups
        - Calculations
    - One Format Phase currently runs for each Extract Work File. 
      - In the new design, the Format Phase would run once for each view. 
        - These executions could be:
          - In multiple jobs.
          - In multiple steps in a single job. 
          - In a single step, with some driver program calling MR95 once for each view.  
          - MR95, running each view as a separate thread in parallel.
      - Rather than making one SORT control statement file for each Extract Work File (as is done currently), MR95 would create a separate SORT control statement file for each view.
        - This would allow the key length to be tuned for the view, unlike now, where the key length must be the maximum of all the views in the Extract Work File.  
    - In an initial design, the SORT steps could be standalone, creating a sorted file to be consumed by the subsequent MR95 Format Phase step.  
      - In an enhancement, we could figure out how to pass the sorted output to MR95 in memory (perhaps by calling MR95 as an E35 (write) exit) to save on I/O.  
    - Open issue: 
      - Should SORT or MR95 do the aggregation? 
        - I suspect that SORT would be more efficient at that.  
        - If we let SORT do the aggregation, then MR95 just reads what it thinks are detail records - no different from now.  
          - Then we're able to use all the features we use now for Extract-Phase views (including read exits, lookup exits, etc.).  
        - We may want to perform some actions before aggregation.
    - There may be some advantages to retaining our standard Extract Work File format as a file interface between the Extract Phase and the Format Phase.  
      - We can gain efficiencies by ensuring that our CT columns remain in an array at the end of each record. 
        - We can guarantee that each number aligns on a double-word boundary.  (I'm making the assumption that we'll be changing the format to use 16-byte decimal floating point numbers instead of the current 12-byte packed numbers).
        - We could add a standard column for the count of records in each sort break. 
          - Then we could use this to calculate averages.  
        - Or, instead, this could be a special accumulator in MR95 that is available for calculations.
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
