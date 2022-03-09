# Meeting notes TSC January 11, 2022 (US)

All interested in GenevaERS development are welcome to join.

## Conference call details

### Zoom Meeting

https://zoom.us/j/2181293577 Meeting ID: 218 129 3577  

## Mentorship
Further discussion regarding requesting a mentee.

Possible work:
* writing COBOL to create the same outputs as the GenevaERS views
* code something to convert the Virginia data to be more mainframe friendly
* build out testing automation via java or
* using Zowe CLI

Current test automation uses FTP. The Zowe CLI can script the automation and have the tests executed on Z. This work may also benefit the Zowe project, we can contribute if we find bugs, etc

The Zowe option received the most votes. Sandy will submit the spreadsheet for requesting a mentee

Considerations:
* since the spring mentorship is for college credit, the GenevaERS project would have to provide guidance, mainframe time, etc. Does the project have the COBOL experience needed to dedicate to the mentee?
* can we request a mentee with COBOL skills instead of using time to train someone up?

Possible work for a mentee; gathering and comparing runtimes for GenevaERS vs COBOL processing of data

## Agenda
### Demo system review
The demo system needs to be reviewed for an improved experience that would allow the project to have greater confidence in introducing to potential users
* PE
* Configuration (script, metadata)
* Workbench
* Instructions / metadata

Current demo does not need the workbench. XML is provided to run the demo views through the performance engine

* An improved demo should have users install the workbench and postgreSQL database
* Documentation should be reviewed for broken links
* Documentation should also be reviewed from the perspective of a new person

The group decided that 3 months would be the timeframe for this work and the first step would be to perform gap analysis on the current demo

Driver for this work.
There is someone who has been participating in R&D sessions that may be willing to talk to his customers about our project. He could be an advocate for GenevaERS. He's very technical. We want the demo to be something that could build confidence in the project

## R&D
The meeting on January 18th (US) will begin an hour earlier and be an expanded demo working session. Ian would like to show the results of his work with Venkatesh earlier this morning and have someone else build their own workbench

## Build
Randall stated that his work will impact the internal, public (GenevaERS), and client (SAFR) builds

## Website updates
Andrea modified the website front page section where blog postings were shown in a "card" style. Instead of using a WPBakery element, a different plugin was used. The results in a smaller footprint for this section of the front page

## Misc
The article Kip wrote for Enterprise System Journal referenced in the TSC meeting November 11th, 2021 has been received and read. They liked what Kip submitted

There is a TAC meeting this Thursday the 20th (US). The Open Mainframe Project is working on finding funding by adding more sponsors. This would allow for installation of the OPM's mainframe that will host most of the OPM projects