Meeting notes from the TSC held on September 8th, 2020. All interested in GenevaERS development are welcome to join.

## Agenda
* Technical Debt listing, and third party licenses and versions
* Hardware access status
* jdbc driver and database selection
* Documentation and getting started guide
* Governance documentation and approach
* CII Badge Prioritization
* R&D Efforts, Spark Integration

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

## Attendance
Voting member rollcall:  
[x ] Randall Ness, IBM (RN)  
[  ] Jeff Horner, IBM  
[x ] Gillian Hannington, IBM  
[x ] Ian Cunningham, IBM (IC)  
[  ] Eugene Morrow, IBM  
[x ] Bob McCormack, IBM  
[x ] Kip Twitchell, IBM (KT)  

## Other Attendees
Jim Hladyshewsky, SAFR Delivery Manager, IBM  
Andrea Orth (AO)  
Randy Peterson  
Sandy Peresie  

# Minutes

## Open Mainframe Summit
* Kip did an online interview with Wsapnil Bhartiya as part of the [Open Mainframe Summit](https://events.linuxfoundation.org/open-mainframe-summit/). 
* Kip is going to create some videos for the summit. 
* The [Open Mainframe project](https://www.openmainframeproject.org/) will build GenevaERS a landing page off of the Project menu  

## CII Badge Prioritization
* There are security [CVEs](https://cve.mitre.org/) in the current version of the workbench. Not practical to fix as this version of the workbench is only going to be maintained before being replaced by the new future state Groovy Geneva Workbench.
* Because the workbench compiler is 32 bit, a 32 bit Eclipse workbench has to be used. The version of Eclipse that the current workbench is using has CVEs.  

## R&D Efforts, Spark Integration
* Sandi and Kip did a review of the Spark integration
* Someone at IBM has taken interest in getting the ZPDT tool up in running  

## Prioritization 
* The project is working through the [TSC checklist](https://github.com/genevaers/community/tree/master/tsc)  

## How to Enable Contribution
* Discussion on how to enable people to use what exists while the project makes changes which would allow parallel tracks of work.
* How do we get to a path of getting real code out for people to contribute to?
    * We can put out demonstration builds which would not be under the Apache 2 license.
    * Ian is hoping to get a Postgres jdbc version working in the next week or two. This would allow a workbench that can create / modify metadata and views  

## Technical Debt
* JDBC driver issue
* Workbench compiler is a 32 bit dll, which require using a 32 bit version of the Eclipse based workbench
* CVEs in the workbench
    * The CVEs are in a part of the workbench which is not used. An approach is to document for transparency

## Hardware access status
The project has been given access to VPN and a LPAR. Bob has been able to log in. The binaries for DB2 are there.  

## Architecture discussion
* There was a refresher on the slide deck Randall showed at the previous TSC meeting. Randall had made some changes and wanted to discuss amongst the group  

There could be an intermediate version; v4.19. In this version, all of the c++ code would be deprecated and the functionality would be replaced using Java. A new test framework and flow analyzer would replace the current debugging tools such as VDP Analyzer and Logic Table Print. The back end would remain the same.

Version 5 could flow from v5 on z/OS to v5 Linux on Z to v5 java virtual machine. The assembler programs would be changed to use Linux on Z system calls.

Comments 
* Between v4.18 (current state) and v4.19, MR91 could be moved to the backend and MR91 could consume an output from Java.
* Both versions v4.V18 and v4.19 options could support DB2 or Postgres as it's metadata database. 
* Enabling development note, Ian has XP (Extreme Programming) experience and Andrea is a Scrum Master. Something to think about for the future.

Reminder, the next TSC meeting on the 22nd will have a 30 minute extension to discuss architecture
