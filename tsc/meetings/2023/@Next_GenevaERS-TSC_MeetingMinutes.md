# Meeting notes TSC 2023-11-7 6pm Pacific Time (US)
All interested in GenevaERS development are welcome to join.
## Conference call details
### Zoom Meeting
https://zoom-lfx.platform.linuxfoundation.org/meeting/95522057563?password=a2cb4656-98bd-4f6e-9d48-2998457acf72
## Attendees 
- Andrea Orth
- Bob McCormack 
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

### Misc

High scan finding [issue 234](https://github.com/genevaers/Community/issues/234)

Before end of year review committers csv and open issues in Community

- Help manually resolving dependencies stopping Markdown Test build process
  - See issue in Markdown-Test repo  
  - https://github.com/genevaers/Markdown-Test/issues/58
## Infrastructure
## Run-Control Apps
## Workbench
- If you manually make the LR inactive then the dependent Views and Lookups are made inactive.
  - Associating or deleting a lookup exit with an LR does not change the state of the LR.
  - Is this a bug or a change in behavior?  What do we want to do?
## Performance Engine
- Alternative to MR88 for GenevaERS V5
  - Remove hardcopy reports.
  - Remove multi-level aggregation.
  - Focus on .csv output.
  - Options:
    - Rewrite in Java.
    - Add features to MR95 to support MR88 functionality.
    - Have MR95 output SORT control statements.
- MR95 parameters to support table lookups using a hashing algorithm  
- Java bytecode 
  - What is the minimum possible bytecode program we could develop?
    - "HELLO WORLD"
## Potential users (who may want support)
## Demo
## Documentation
- Technical documentation 
- "A document a week, that's all we ask" 
## R&D Work
- Sort utilities for UNIX 
- Byte Buddy 
- Liberty - open source alternative to WebSphere.
## Conferences 
- Possible presentation at the Winter SHARE conference 
## For next time 
