# Meeting notes TSC 2024-07-16 6pm Pacific Time (US)
All interested in GenevaERS development are welcome to join.
## Conference call details
### Zoom Meeting
https://zoom-lfx.platform.linuxfoundation.org/meeting/95522057563?password=a2cb4656-98bd-4f6e-9d48-2998457acf72
## Attendees 
- Andrea Orth 
- Gillian Hannington 
- Ian Cunningham
- Kip Twitchell
- Michael Shapiro
- Neil Beesley 
- Randall Ness
<!-- 
- Bob McCormack 
- Eugene Morrow 
- Jeff Horner 
-->
## Run-Control Apps
- Run-Control Generator
  - Feature that allows external preparation of RED files 
    - No JLT view?
    - XLT to use what would be the LR if it were generated.
    - Do we generate variants if and when key values or effective dates vary
    - No REH entry is written? 
      - That is done externally?
    - As an aside should we have the code that generates the header entries?
  - Are there any open issues about date processing?  
  
## Development 
- Review the release procedures proposed by Ian. 
  
## R&D
- Kip and Neil
  - z/OS Java interlanguage R&D by GenevaERS 
    - Run Control integration
    - Java integration

## Documentation
- Prepare for OMP review. 

## Workbench


## Administration

IBM Tech Xchange 2024 Oct 21-24
June 15 is the deadline for submission to OMP. The [submission form](https://bit.ly/3Ur9lCj) is a custom OMP form
We could submit something and if not selected or plans don't work out, we can ask OMP marketing to identify an appropriate outlet for a video on the topic.

OpenSSF badge
Add Kip as backup after ownership is changed
Ian is going to try contacting Bob so someone else can make badge updates

### Items for focus in 2024

#### The road to gold
Andrea updated Code of Conduct. Currently in a dev branch.
Quick check in on roadmap and architectural design doc.
* Roadmap still in Randall's queue
* Team decided that design documentation should capture the future state design. No value in capturing current state since the future state changes will be released. Ian plans on using Javadoc for workbench and runcontrol design docs.

## Misc

Documentation updates should run parallel to development.
Internal discussion if the DB2 scripts should be released as open source.

## 2024 goals

- Product Research
- ADABAS support
- Changes to MR88
- Stretch goal of updating documentation to reflect current functionality

### Project lifecycle procedures
## Infrastructure
## Run-Control Apps
## R&D Work
- Using ADABAS as a data source.  
- Alternatives to a using a database for metadata
- Byte Buddy 
- Liberty - open source alternative to WebSphere.
## Performance Engine
- Aggregation functions
- MR95 parameters to support table lookups using a hashing algorithm  
- Java bytecode 
  - What is the minimum possible bytecode program we could develop?
    - "HELLO WORLD"
## Potential users (who may want support)


## Conferences

- Open Mainframe Summit again partners with the [FINOS](https://www.finos.org/) conference in New York 9/30 - 10/1.
- There is also a conference in London 6/26 - London Finance Forum

## For next time 
- Kip will discuss AI on the mainframe.
- Randall will compare MR95 to CICS. 
