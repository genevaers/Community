#### Review the repositories, including the repo document and clarify what is stored in each rep

* There have been some discussions in recent daily status meetings regarding the different GitHub repositories and what is stored in each repository. Also, it was unclear to some project members if the repository matrix still accurately reflected which repositories have been created. It was shared that rows 8 through 11 do accurately reflect that those repositories have not been created yet.  

**Action Item**
* Before the next TSC meeting, Bob will update the REPOS.csv file and we can go over what each repository is for.


* Regarding the work going on in the internal IBM GitHub repositories, the gradle based test framework needs some massaging regarding credential management and needs to be pointed to the Vicom Infinity mainframe.
* The workbench code builds. Bob is running licensing scans on the code. When this is complete, the code can be moved to one of the project GitHub repositories and scanned by John.


#### What gets stored in Google Drive

This agenda item spun out to multiple discussions and a direction not determined regarding Google Drive. The documentation discussion is captured in it's own section below.

There are some documents such as slide decks, spec documents that are in Microsoft Office documents. Where should these be stored; Google Drive or GitHub?

GitHub is designed for code, it can store documents in formats that are not code such as Microsoft Office documents, but none of the features GitHub has built in for code applies to Office documents. Office documents are stored in a blog and cannot be versioned, diffs can not be performed on them. There is an advantage for spec documents that they could be stored close to the code. There was also a discussion of executables, which also could be stored in GitHub or some other location.

#### JIRA
Sandy gave an update on our new JIRA instance. We currently have two projects; a software project and a business project for outreach. The software project comes with a Kanban board which, to some degree, can be customized. The business project does not come with a Kanban board. There is an issue that by default, the Kanban board does not allow for the due date field to be defined or edited. Only someone with global permissions, which we do not have, can make due date an editable fieds. Sandy opened a ticket to the Linux Foundation to change this and expects to hear back in a week, week and a half.

Sandy and Andrea each created Epics in JIRA. An Epic is at the highest level. Epics can be grouped in the Kanban board. Bob will move his GitHub project board items to JIRA.

[Link to the software project in JIRA](https://jira.openmainframeproject.org/secure/BrowseProjects.jspa?selectedCategory=all&selectedProjectType=software)  
Login credentials are the Linux Foundation credentials that would be used for the project mail list and calendar.

**Agenda item**  
Next TSC Meeting is for the group to decide what columns we want on our board

#### Public zO/S Cloud Update
There is currently a working group studying how to make it easer for organizations and companies to donate MIPS. One issue is that some organizations, for example universities, may not have experienced resources that know how to setup, define LPAR(s), and make it secure, etc. Also, the pool of mainframe sys programmers is not large enough to support donated mainframes or MIPS. Can automation scripts be created that would fill these gaps? Also, to capture pain points, a poll or some other method will be used. Basically, TBD.

Bob pointed out, that internal to the mainframe, there already is a level of automation. This automation tooling is proprietary to the mainframe. Bob was going to follow up with Kip on this.

Soon, there will be a GitHub repo for this working group. The POC will be automation beginning with USS.

#### Spark Update

Neil provided an update on the Spark work on the internal IBM instance the project has been provided. Issues getting through to the instance via PUTTY and USS did not work, Bob will try using Putty and if he also can't get through will have the matter fixed.

#### Workbench Update
Workbench update was provided during the first agenda item which is at the top of these minutes.

#### Performance Engine
* Ian has been working on refactoring MR91
* There has been a change made to MR95 making it easier to create mainframe dump files
* Gillian working through the performance engine to improve error messages and add consistency

#### The March to March
Kip would like to see the project move from Incubation to Active by March 4th. This requires meeting the items in the checklist including the CII Badge. What remains of this work?

Bob explained that the bad is "self certifying" and for some items, we will note what we will do to meet the requirements. Bob thinks we will meet the aspirational March 4th date.

**Action Item**  
Bob will go through the checklist and update JIRA

#### Documentation Discussion

There was discussion regarding the file format of the GenevaERS documentation; PDF, Markdown, etc. Eugene thought this was resolved last year with Eugene using DITA to create and output GenevaERS documentation. There was also discussion of where the final documentation should go; web page, google drive, GitHub pages, embedded in the software. No decision was made.

Action items that came out of the discussion:
* At this time, Eugene only as SAFR versions of the documentation, no documentation that is GenevaERS branded.
* Eugene may need to use an open source tool to generate documentation.
* We need to determine what our first cut of GenevaERS documentation will be.

Eugene noted that not all of SAFR / GenevaERS has been documented. A possible short term solution would be to line up knowledgeable  parties and screen record discussions. Gaps could be captured in this manner and the community could fill the gaps of creating formal documentation.

#### Misc
Also discussed during this time was an email from Vicom Infinity regarding setting up our USS instance. The team discussed and decided on the sizing of the instance so Randall could respond to the email.
