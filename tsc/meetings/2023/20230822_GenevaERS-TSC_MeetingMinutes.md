# Meeting notes TSC 2023-08-22 6pm Pacific Time (US)
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
- Jeff Horner 
- Kip Twitchell 
- Michael Shapiro
- Neil Beesley 
- Randall Ness
## Administration
- Annual review approval - waiting on approval via email
- Annual Review video for GenevaTV in progress
- Kip's link to the WordPress website admin is no longer working
- Change "The GenevaERS Museum" to "GenevaERS Evolution" on genevaers.org
## Infrastructure
The following repos have Dependabot alerts - all are in Gemfile.lock
- User-Documentation
- Workbench
- Demo
- Markdown-Test
## Run-Control Apps
## Workbench
- Should the GenevaERS compiler be embedded in the Workbench? 
  - ****
- Why must a lookup be in Active status in the target environment for migration to succeed?
  - **We don't know, but we're not going to change it for WE 4.20.**
- Is there a plan to rewrite Migration?
  - **No.**
- Architecturally, should we head away from using databases and just save text files instead? 
  - **Pro**
    - **Can keep text files in a source control system**
      - **allows you to see changes over time**
    - **Eliminates dependence on database management**
  - **Con**
    - **Major change**
      - **need to develop design for metadata dependencies**
## Performance Engine
## Potential users (who may want support)
## Demo
## Documentation
- Markdown test static site no longer exists. Is this expected?
  - **Andrea will look into it.**
- "A document a week, that's all we ask" 
## R&D Work
## Conferences 
- Possible presentation at the Winter SHARE conference 
## For next time 
