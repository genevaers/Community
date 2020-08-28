Meeting notes from the TSC held on Aug 11, 2020. All interested in GenevaERS development are welcome to join.

# Agenda:

Proposed GenevaERS 5.0 Architectural Direction  
Logo Adoption and Marketing Update  
Shared System Access  
Getting Started Guides  
Joining the Project  
GenevaERS Installation and Use  
Source Code Release, Evaluation Version and zIIP removal  
Spark POC  
Round table  

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

## Attendance
Voting member rollcall:  
[x ] Randall Ness, IBM (RN)  
[x ] Jeff Horner, IBM  
[x ] Gillian Hannington, IBM  
[x ] Ian Cunningham, IBM (IC)  
[ ] Eugene Morrow, IBM  
[x ] Bob McCormack, IBM  
[x ] Kip Twitchell, IBM (KT)  

## Other Attendees
Jim Hladyshewsky, SAFR Delivery Manager, IBM  
Andrea Orth (AO)  
Sandy Peresie  

# Minutes

## Proposed GenevaERS 5.0 Architectural Direction

Randall presented his slidedeck which captured:  
* Current State
* Pros and cons of remaining on current GenevaERS architecture
* Possible Future State; GenevaERS 5

A great deal of discussion occured around future state. 

A proposed first iteration of GenevaERS 5 would be to keep the backend "as is"; C++, COBOL, and Assembler while having a more modern front end coded using a "variant" of the open source language Groovy; aka "Groovy Geneva".  

In this solution, the free software code editor VSCode would become the IDE for the new "GG Studio". GG Studio is a separate entity from the proposed "GG Source Code".  Using current state terminology, GG Source Code would be such things as the LRs, Lookup Paths, etc. The run control files; JLT, XLT, VDP creation would be initiated by the front end. Open source tooling Gradle would be the technology behind the scenes creating the run control files.

Future iterations would include the capability of custom front ends. A simple synopsis was "All the power of Geneva with whatever front end you want".  

There was a callout to Open Mainframe Project [Polycephaly](https://www.openmainframeproject.org/projects/polycephaly). Polycephaly is built using Groovy and provides developers modern tooling options. It removes the need for separate development paths for distributed and z/OS workloads. Developers can develop on any platform, store to Git and use Jenkins to deploy.

This project has had some preliminary discussions with the Polycephaly project.

The action item for this Geneva 5 discussion is to setup a cadence for a series of architectural meetings.  

## Logo Adoption and Marketing Update  
Multiple people liked / could go with concept 1A; options can be seen in the GenevaERS Slack channel. Sandy would like the logo slanted forward to indicate speed. Action item after the meeting was to ask John Metric if we could have the logo modified to slant.  

## Shared System Access  

Vicom Infinity is a sponsor of the Open Mainframe Project and has offered a shared LPAR for us to use. The LPAR has 2 processors and may not have DB2 started. Members of this project may need to help getting DB2 up and running on this LPAR.

5 user IDs were requested today for this instance. It may be next week before we get access. We will also be given a VPN to get into Vicom Infinity's network. We could then connect the current version of the SAFR/Geneva workbench via JDBC and run the batch workflow.  

## Joining the Project  
* Sandy is working on a Joining the Project Guide to aid in demystifying all the signups, etc that is necessary to follow / contribute for the project. 
* Andrea added a new menu option called Community on the GenevaERS website. The menu contains options for the mailing list, Calendar, and GitHub Community repository.

Kip did a short explainer of the two sets of repositories; IBM and GenevaERS. The repositories under IBM are staging repositories. One purpose is to perform scans to find potential licensing issued for code is transferred to the GenevaERS repository.

## Request for the next TSC meeting

Kip would like to have an uplifting, hopeful opener for each TSC meeting