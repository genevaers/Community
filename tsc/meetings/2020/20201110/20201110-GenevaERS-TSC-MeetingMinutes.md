Meeting notes from the TSC held on November 10, 2020. All interested in GenevaERS development are welcome to join.

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

### Attendance
Voting member rollcall:  
[X] Randall Ness, IBM (RN)  
[X] Jeff Horner, IBM  
[X] Gillian Hannington, IBM  
[X] Ian Cunningham, IBM (IC)  
[ ] Eugene Morrow, IBM  
[X] Bob McCormack, IBM  
[X] Kip Twitchell, IBM (KT)  

### Other Attendees
Andrea Orth, Sandy Peresie, Jim Hladyshewsky, Neil Beesley 

## Minutes

### Mainframe Environment
Kip and Randall have been having discussions with Vicom Infinity. Vicom has a history of supporting Open Mainframe Project (OMP)and currently is hosting 6 out 7 OMP efforts.

The size of our effort and the timeline is not something Vicom can support on their system for the duration of our project.At this time, it is not yet clear how long Vicom will host GenevaERS and what features they are comfortable in letting use. They will still setup a Linux on Z environment.

A gap was identified. The number of mainframe system programmers is shrinking. These system programmers understand how to manage mainframe environment setups.

Kip is having discussions within IBM regarding the need for these kinds of projects to have access to a mainframe. An idea is to suggest a new OMP project with the mainframe as a Platform As A Service (PAAS) model. This would reduce the need for system programmers. Parameters could be set regarding what could be installed and used. Which resources can be consumed. Security and platform stability.

Another gap was identified. Tom from Vicom asked for some documentation regarding the OMP designation as he wasn't sure if the GenevaERS software should be on this machine. Currently, there is no information publicly available. Action item could be to make updates to the GenevaERS.org site and the wikipedia entry.

### Prograss on data
Sandy has been working on getting the reference data files up the the Vicom mainframe. She's run into an issue that they are mac files and Sandy does not own a mac. Sandy has been trying to mount a drive on her ubuntu instance to try to move data from unix to dos and vice versa

Sandy inquired if Bob had been having the same problem. He had not. Bob brought files down to windows, then GitHub, then USS than converted for Z. The data looks like it's comma separated. 

There was a wider discussion regarding the differences between how mac handles end of line versus windows such as carriage return and line feed. This difference makes the reference file present as one record.

Per Kip, in USS, you can set an ISO coding parm on an ISO structure. He has a link to a webx video that he can share with Sandy.

### Workbench Update 
Going well. He has a postgres workbench that will accept workbench XML. Views can be created and activated. He's also creating some postgres SQL scripts so the database on the linux machine can be setup and used with the new workbench. Exporting from this database into workbench XML may have a case sensitivity issue and Ian is not sure that would be accepted. If not, this can be resolved

People can log in and create new things using this postgres version of the workbench. Ian needs some people to try it out and log defects

Kip asked if people can set this up on their own machine with a local postgre database. Yes, Ian can give people a deployable java executable. Ian can walk people through setup after postgres is installed locally. He's setting it up so it can be ran via cmd line and have the postgres database ready

Kip on sharing the executable. Can use Box or via the IBMSAFR repository

Ian also needs to remove the db2 release path. 

Issues found with the new workbench will be opened in the yet to be created Workbench repo. We need a new issue opened with the repos and committers, Community can be modeled off of

We can use IBMSAFR for install instructions and issues. When ready, the code would need to be scanned and put into GENEVAERS Community.

Sandy spent a couple of mornings with Ray. The onboarding document is ready to be forked into the repository and added to website. 
This document will go in the Community repo. Can add a link to the document in the README.md or maybe replace the CONTRIBUTING.md
Sandy will also send the onboarding document to Fatima for review.

Also, Neil and Ray are not members in Community. This is another discussion with john.

### Performance Engine Update 
Still working on testing changes for 64 bit support. Focusing on customer exits which need to be upgrade for 64 bit support.  

The new extract report is quite a bit different than the report used in pervious versions of the performance engine. Gill will be working on documentation explaning the new report along with the parms available when the extract job runs.

Neil on DB2 VSAM. How to leverage reading the DB2 VSAM files is something that IBM no longer provides public information on. An alternative is to use a high speed database unload that can be leverage. We could latch onto an exit and feed the data into memory. MRDV could be replaced with the unload utility based on what the customer whould need.

Also, longterm, the code for DB2 VSAM utilization needs to be removed from the code base so it's not in the open source version of the product. Short term work around is to remove DB2 VSAM from the CODETABLE which would prevent selection in the workbench

### Infrastructure Update 
Bob set up git with RTC at the workspace level. He copied from his git repository clone to RTC and vice versa. No conversion issues occured and data looks like it did within GitHub

The GVBLIB repo in GENEVAERS is not merged into master.

SPARK issue. SPARK used to be bundled into the base mainframe product. It is now a priced IBM product. Bob sent Kip the name of the product owner within IBM for SPARK. We need to find out if there was a way that SPARK could feasible on the Vicom system

Bob is working with Randall on how much space would be needed on the Vicom system. Did a trial of pulling data from Data Work to windows than MVS with a utility conversion subparameter. There is over 10GB of data

### Misc.
Sandy attended zowe TSC today and they offerred a walk thru of what they are doing. They had brought up a couple of packages they are planning on using for their code; Sonarqube, Coverity, Snyk. These are code scanning products