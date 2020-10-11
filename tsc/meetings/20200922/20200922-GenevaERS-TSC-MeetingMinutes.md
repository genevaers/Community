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
Andrea Orth
Sandy Peresie
Elana Schuman

# Minutes

## Open Mainframe Summit update
* community connections   
The summit was September 16th and 27th. There are session videos out on the OMP YouTube channel. Kip and Sandy did the mix and mingle; we have two new members which will be meeting with Sandy at 10 AM EDT tomorrow.  

We had an invitation from Zowe to attend their TSC and architecture meeting. Sandy and Randall attended the architecture meeting today. Most of the meeting was regarding reviewing their proposal as part of TSC work. Sandy got a copy and posted the link in Slack. Sandy thinks it would be useful to have this outline so people understand what we are trying to do.

Can Zowe help us?
Zowe items that could help us:
* Command Line Interface (CLI) - core set of commands for working with data sets, USS, JES, as well as issuing TSO and console commands from a workstation command line interface.  
* Zowe application framework is a web user interface and includes apps for traditional access such as a 3270 terminal, editor, and explorers for working with JES, MVS data sets and Unix system services.  
* API mediation layer containing a catalog of REST APIs and a framework for single signon  
* During Zowe TSC, reviewed a new performance cache API that was proposed

Sandy was asked to focus on making open source connections. As part of that is creating a list of good first issues that people new to the project could work on. 

Open discussion on items that may make good first issues:  
* Release document
* Research on Izoda tooling; what are it's features
* Automated build process 
  * gradle, groovy, Zowe cli, gvblib, run the assembly process for linkedit (similar to a COBOL compile)
  * work on building the security scans 
* New people could review things and provide feedback; is what is written make sense? Review training videos.
* Master the Mainframe hackathon. What problem could be solved?

*Misc
Sandy is the integration architect over open source
Jeff is the Performance Engine architect  

## Project status
* commitment to John Mertic that by the Feb. TAC meeting, GenevaERS will be an Active project (out of Incubation phase) 
This is an aggressive date.  The goal is to become active before the "Death of the Mainframe" date of March 15, 2021 and before the GenevaERS domain renews in April.  

When we become an active project the Linux Foundation will create a LLC for GenevaERS.  

Challenges  
* Getting code out and working. Which means someone can go to our site, clone the repository and have working software and data. An automated build process would not be necessary at this time.

* Kip went through some of the items we have left in the TSC checklist, what wil be challenging is the core infrastructure best practice badge.  

* Also, how can someone run GenevaERS without z?  

Automatic TSC Agenda builder
When an issue is tagged meeting or maybe meeting agenda, the agenda GitHub action scans and adds the item to the agenda.

## Website/Marketing update
There are two bad links on the GenevaERS OPM mainframe project webpage, the GitHub button links back to the OPM main page not GitHub. The chat icon also links back to the OPM mainframe project page and not to the GenevaERS slack channel. An issue should be opened on OPM GitHub to request these bad links get fixed  

Kip created a GenevaTV YouTube channel and will be uploading training videos to the channel. When the channel reaches 100 subscribers, it will get it's own URL  

Kip tried to bid for the Geneva.tv URL, but the price went too high.  

Andrea showed the participants the Geneva.tv channel and went through the GenevaERS website updates  

## Workbench update
* removal of the compiler and postgress progress  
Ian continues work on allowing the workbench to use a postgress database instead of a DB2 database. Ian can create a view, add a column, and activate the view.  Within the next week or so, we may have a draft kind of workbench that can extract views. This version of the workbench can be shared via box so Sandy and Andrea so can begin work on documentation. Neither gradle or VSCode are part of this version. Code still needs to be put into a GitHub repository.  

Some junits will be created by Ian, but any java programmers that may join the project could create more by watching the existing videos and filling in gaps.  

The workbench doesn't need to use the 32 bit complier



  
  
  we dont need the 32 bit compiler dll, we can use an antler (4) ...   for a self contained java workbench. might need to watch video about 50-60 min in on this section.  
  once we get here, current eclipse version is luna and has multiple cves. latest eclipse just released in june.
  
 
  
## Performance Engine update- Gill  
* zIIP removal  
  zIIP code is peppered throughout the peformance engine. not it's all sep, it can be linked in if available for ziip usage if conditions are met. if not linked in, it will carry on as normal. done, needs some vigorous testing.


## Infrastructure update 
This topic was moved to the Infrastructure meeting which takes place after this meeting 

## Spark and OSS integration
Jeff and Neil

java assembler integration - wanted to leverage going to have to watch the video here
mr88 or mr95? / aggregation phase - java jni out of the box generates an out of the box wrapper, or ascii / ebdcic converstion 
David....... got the longfellow wrote an article working off of / inspired by


## other
Kip proposed changing the dates of the TSC meetings to the 2nd and 4th Tuesday of the month
