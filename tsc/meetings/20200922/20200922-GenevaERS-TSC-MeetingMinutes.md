Meeting notes from the TSC held on September 22nd, 2020. All interested in GenevaERS development are welcome to join.

## Agenda
Randall will open  
Open Mainframe Summit update - Sandy   
  * community connections 
  * Zowe connectivity 
  * Polycephaly 

Project status - Kip  
  * commitment to John Mertic that by the Feb. TAC meeting, GenevaERS will be an Active project (out of Incubation phase) 


Website/Marketing update - Andrea   
  * New theme 
  * New YouTube channel  
  * Domain name renewal - April 

Workbench update - Ian   
  * removal of the compiler 
  * postgres progress

Performance Engine update - Gill  
  * zIIP removal 

Infrastructure update - Bob  
  * Zowe availability 
  * new GenevaERS Infrastructure meeting to follow this one 

Spark and OSS integration - Jeff and Neil  

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

## Attendance
Voting member rollcall:  
[X ] Randall Ness, IBM (RN)  
[X ] Jeff Horner, IBM  
[X ] Gillian Hannington, IBM  
[X ] Ian Cunningham, IBM (IC)  
[X ] Eugene Morrow, IBM  
[X ] Bob McCormack, IBM  
[X ] Kip Twitchell, IBM (KT)  

## Other Attendees
 
# Minutes

## Open Mainframe Summit update
* community connections   
sept 16th and 17th, there are session videos out on the omp youtube channel. kip and sandy did the mix and mingle and as a result, we have 2 new members which will be meeting with sandy at 10 am EDT. hoping to get more engagement in area that looking for work. had an invitation from zowe to attend their tsc and architecture meeting. which sandy and randall attended the architecture meeting today. most of the meeting was regarding a proposal, sandy got a copy which i think is in slack. sandy thinks it would be useful to have this outline so people understand what we are trying to do. randall was impressed, zowe was very profressional

sandy was asked to focus on making open source connections

can zowe help us?
they have a ... see screenshot

good first issues - getting people engaged. created an issue in the community github. what are things people can help with without knowing much geneva?
what are some of the things we can look at?

open discussion
tsc checklist? release document, infrastructure, research on Izoda - SPARK toolingwhat is it main features, automated build, (gradle, groovy, zowe cli etdc)gvblib source for automated builds - run assembly process for linkedit (like cobol compile), what process do you think to automated a build,security scans (may attract more people from an open source background who could bring , training videos, web.
may be a part of the master the mainframe, hackathon - what could our focus for the hackathon be? what problem to be solved. mtm content and what could they do.context is that we are too light on resources to do a genevaers hackathon. they could review things and provide feedback, does it make sense.

integration architect over open src - sandy
jeff is PE architect

  * Zowe connectivity 
  * Polycephaly 

## Project status
* commitment to John Mertic that by the Feb. TAC meeting, GenevaERS will be an Active project (out of Incubation phase) 
challenges - getting code out there and working. what does it mean to have the code working? having the code out their. may not have an automated build process via github. go to our site, clone, download have working software and process thru data

maybe a shortcut

we met with john m. last week. feb date is perhaps aggressive. death of the mainframe data is march 15. 2021 and domain renews in april.

kip went through some of the items we have left in the tsc checklist, hwat will be challengeing is the core infr best prac badge, critical. nothing in the tsc list directly says something that we have to have something that works. tsc may have been built with linux in mind, not mainframe

note the proposal above is part of tsc

how can someone run it without z?

meeting agenda or whatever the label is - the agenda build github access scans and adds something to the tsc issue - research github actions

when we become an active project a llc will be created for us

## Website/Marketing update
press relse info
open an issue for opm github link issue
add slack to chat, also opm slack link doesnt work either
kip will upload training videos to geneva.tx
when we get 100 subscribers, we get our own youtube url
mae
geneva.tv, bids got too rich

## Workbench update
* removal of the compiler 
  * postgres progress
  Ian, moving the workbench to run on postgress db. ian can create a view, add a column, and activate the view.
  we dont need the 32 bit compiler dll, we can use an antler (4) ...   for a self contained java workbench. might need to watch video about 50-60 min in on this section. within next week or so, have a draft kind of workbench to extract views. still need to put code into github
  once we get here, this internal version can be shared via box so sandy and i can begin wking on documentation. gradle not part of this version, current eclipse version is luna and has multiple cves. latest eclipse just released in june.
  
  creating junits to exercise this could be good for any java programmers that may join. could someone watch the videos and create junits. there are already example junits
  
  vscode is future state
  
## Performance Engine update- Gill  
  * zIIP removal 
ziip code is peppered thru the pe.not it's all sep, it can be linked in if available for ziip usage if conditions are met. if not linked in, it will carry on as normal. done, needs some vigorous testing.

## Infrastructure update 
This topic was moved to the Infrastructure meeting which takes place after this meeting 

CHECK OFF MARKETING STUFF IN TSC LIST

## Spark and OSS integration
Spark and OSS integration - Jeff and Neil  

java assembler integration - wanted to leverage going to have to watch the video here
mr88 or mr95? / aggregation phase - java jni out of the box generates an out of the box wrapper, or ascii / ebdcic converstion 
David....... got the longfellow wrote an article working off of / inspired by


proposed sch change tsc 2nd and 4th tues instead of every other week
