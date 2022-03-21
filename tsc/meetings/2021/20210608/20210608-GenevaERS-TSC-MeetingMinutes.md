Meeting notes from the TSC held on June 8th, 2021. 
All interested in GenevaERS development are welcome to join.

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

### GitHub Project Management ####

* Issues in local repos can be aligned with the top level Demo project which is at the GenevaERS organization
* Agreed that the issues for the Demo work would be placed at the top level Demo project.

### Demo progress ###
#### Executable - PE & WB ####

* Gillian is working on a sub-module that gets pulled in at link time. She thinks she can finish up the work today. 
* Need to sort out which modules get the Apache license vs the IBM copyright notices
* After the above work is created, a copy will be made of the library and the items that don't belong in Demo will be stripped out
* Eugene can then do a build and Randall would like people to review before placing in public GitHub
* Short term, the code will be placed in the IBM SAFR repo

#### Public Postgres database & database scripts ####

Not much progress to report. While nothing came from two recent approaches, there may be some future developments regarding a public postgres database. However, Kip does not have a sense of when things will happen

#### Sample views in XML format ####
During Friday's R&D session, several views were built. Neil went ahead and ran them. They ran as expected

#### Documentation & Demo video updates ####
* Randall is going to capture the steps for downloading and installing the modules and unpacking them on a mainframe
* Documentation for downloading and installing the demo will go in the Readme.md file in the Demo repo
* No progress on demo video

Regarding documentation in general - Randall noted that he has documents in Microsoft Office formats and it would be best if these were converted to a more accessible format like Markdown. There is software that can convert office documentations to markdown. He also thinks there is a benefit of using .csv files instead of building table in markdown files. Benefits - A variety of software can read .csv files and the files can be embedded in pages

#### Sample REF & event files ####
Do we provide anything more than providing the files?
* People would load them onto their machine using tooling and setting required by their mainframe environment

Should we provide documentation such as
* Instructions if using SSH
* Instructions if using FTP

Ian pointed out that the test framework has java files that will transfer the JCL and workbench files to the mainframe

#### Misc ####
* The demo workbench will be placed in the public IBM SAFR repo
* Run control - processing lookup logic and generation lookup function codes
* Gillian also has some messages in the code to finish cleaning up
* We have an IBM SAFR trial license which would incorporate all of the GenevaERS Apache licensed code and the IBM copyrighted code

### Mentorship ###
Deb has taken a new job and will not have time to be a mentee. He does still want to be involved.

This topic had a discussion of who to target with this project; mainframers or non-mainframers.
Mainframers have the data and problems that Geneva can solve. But in Kip's experience there is more interest in the project from people interested in open source / non-mainframers. So far, the two new people who have been interested in working on the project, do not have mainframe experience

