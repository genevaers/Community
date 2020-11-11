# Agenda
## Issues
* Access requests #66 and #67
* Issue #64 - John's suggestions
* If time other open issues

### Workbench Update - Ian, 3rd item

### Performance Engine Update - Gill

### Infrastructure Update - Bob

### Recruiting Update - Sandy

## Infrastructure

### GIT to RTC synchronization

### GIT Clone on VICOM

### GVBLIB Merge done and we wait on a SPM PTF for HLASM Toolkit

### Use of SPARK

### Spacer on VICOM and World Data

## mainframe Environment, first topic
Kip & randall. Vicom infinity. has 6 or 7 omp projects on their system
kip discussing with ibm regarding the need for these kinds of projects for the mainframe. gap - the # of system programmers is a gap. this aspect of shared environments in people, touches a nerve in some people. what's needed is to perhaps suggest another opm project with PAAS - mainframe as a service which would reduce the need for system programmers. parameters can be sent regarding what can be isntalled and used, what resources can be consumed, security, and platform stability. 

size of our effort along with timeframe is not something vicom alone can handle. a bit of limbo for how much and how long vicom can handle.

tom was hoping we could provide some documentation for the opm software designation, wasn't sure if he should even have the software on his machine. could add clarity on website. "we are an official open source project..." it someone goes to genevaers.org make more clear also wikipedia entry update. tom is interested in seeing what kind of synergy we can provide vicom.

no clarity oin what they can provide us and what they are comfortable allowing us to use

linux on z will still be stood up

## Progress on data  - Sandy, 2nd item
getting one of the reference data files up to the mainframe. they are mac files and sandy has a windows machine, not a mac. Sandy is trying to mount a drive on her ubuntu instance to try to unix to dos and vice versa

Bob, hadn't had issues moving to github site. does not have mac either. moving from github to z, a converstion is on place for data and members of a repository. per sandy, the virginia data is in mac format. bob brought it down to windows, then github, then uss, than converted to zos with a converstion parameter. looked like comma separated. it's the end of the line, such as carrage return / line feed. all the reference file comes off as 1 record. kip - in uss, you can set an iso coding parm on an iso structure. he has a link to a webx video that he can share with Sandy.

## workbench update - ian
going well. he has a postgress bench that will accept wkbench xml and create views and activate them. also creating some postgress sql scripts so the dbase on the linux machine can be setup and used with the new wkbench. exporting from this dbase into bench xml may have a case sensitivity issue and ian is not sure that would be accepted

can log in and create new things

ian needs people trying it out - good first 

kip, can people set this up on their own machine with local postgress? ian can give a deployable java executable. ian can walk people thru how to setup after postrgress installed. he's setting it up so it can be ran via cmd line and have the postgress dbase would be ready.

kip - sharing the executable. via box or on ibmsafr eval copy executables.

ian needs to remove the db2 release path. kip to randall,

send ian an email with a time for install

issues will be opened under workbench repo, which needs to be created

we need a new issue opened with repos and committers, see community. we can use ibmsafr for install instructions and issues. when it's ready, code would need to be scanned and put into community

github issues as we find them.

not to self, install postgress

Sandy spent a coouple morning with Ray. it's ready to be forked into the repository and added to website. this is the onboarding document. and go in community repo. can add a link to the doc in the readme, maybe replace the contrubuting.md. she will also send to fatima for review.

seq to an issue, neil and ray are not in the community project. if you look under project then people, neil is not there. another discussion with john.

## PE update - Gill
still wking on testing changes for 64 bit spt. focusing on customer exits shich need to be upgraded for 64 bit spt. there are quite
the ext rpt you get generated is significantly changed since previous vers. she will be working on documentation explaning it and ext job parms. knowledge transfer regarding a member that is retiring. 

neil, we could do diff things. like a high speed dbase unload can be leveraged. we could latch onto the exit and feed the data into memory. replace mrdv with the unload utility of your choice based on what a customer would have / need - longterm vision
per randall, we do want to extract the code regarding dv2 vsam so it's not in open src. short term would be to remove from codetable so people could not select it. 

## bob - infrastructure update
per randalls instructions, sync up git with rtc at the wkspace level. copied from clone of git repo to rtc and vice versa. no conversino issues and data looks like it did within github scm instance. gvblib repo in genevaers is not merged into master. 
spark - was discontinued with ibm and now bundled with a priced ibm product, zed? bob sent kip the name of the product owner
spark itself is open src. bob and kip discussed an approach with product owner. trying to drive experimentation on the mainframe, what was ibm hoping to achieve. 
spark processing - large amt of data, wking with randall how much space would be needed on vicom system. did a trial of dataworld to windows than to mvs with a utility with a covnerstion subparameter. +10gb of data. but would need to lknow if spark on z would be feasible on vicom systme

ahve a ptf for hi level assembler toolkip which would allow for ur30 on vicom

kip in conclusion
great acticity, the issues running into are things we want to solve 


sandy attended zowe tsc today and they offerred a walk thru of what they are doing. they had brought up a couple of packages they are planning on using for their code. sonar, sonarcube,coverity, snik? spot errors might be like coverity which runs as part of the build pipeline