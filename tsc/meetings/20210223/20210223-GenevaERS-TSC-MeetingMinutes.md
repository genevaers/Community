Meeting notes from the TSC held on February 23rd, 2021. All interested in GenevaERS development are welcome to join.

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

## Attendance
* Randall Ness
* Gillian Hannington
* Ian Cunningham
* Bob McCormack
* Kip Twitchell
* Andrea Orth
* Sandy Peresie
* Neil Beesley
 
# Minutes

## Documentation Approach
Deferred to next TSC as Eugene could not attend this TSC meeting.
Eugene did see Ian's static site using Gatsby and is happy with it.

## Password Removal - Ian
Currently, the way passwords are handled by the workbench do not meeting the Badge CII criteria.

Ian proposes that we don't store passwords in the workbench for connecting to the database. The workbench would just login using the credentials entered by the user into the workbench.

The other password is used for metadata protection and isn't necessary.

If we think of the workbench editor as just a code editor, the Geneva "code" would be imported via XML, modified, saved, exported, and could then be stored in a source code repository such as GitHub. The editor would work like other code editors such as Visual Studio.

If there is a database behind the workbench, the user would have to enter their mainframe database credentials each time.

We have recognized, over time, using GenevaERS for source code management is a high bar when the GenevaERS XML could be stored in an external source code repository like GitHub.

Currently, the GenevaERS XML has the LR as an entity in isolation from other users that could be making changes to a LR that is shared.

Proposal - Disable password prompt in the workbench which disabled, as in not calls, the workbench password code; everyone would be an administrator in the context of the current workbench.

This would be the 2nd instance of breaking backwards compatibility with the current product. The removal of hardcopy reports being the first

Committers on the call voted for the following proposals
#1 Users have to type in their database credentials instead of the credentials being stored in the workbench
#2 The workbench user password would be disabled and the editor becomes more like a code editor with code being imported into the workbench

Both proposals were approved and Ian will update issue #99 then close

## Source Code Update
John M. gave us permission to populate directly into our repos.

Performance Engine - Bob is waiting on Randall to come up with specifications on which modules end up in GenevaERS vs SAFR
Gillian - there is a bit of work to be done regarding DB2 VSAM code that needs to be cleaned up

Ian - has 3 repos.
Frontend - MR91 (run control), the flow analyzer, and LT print which are coded in Java. The other reports are the workbench and the test framework. Ian has integrated RAT into the Gradle builds.

## Blog post for Open Mainframe Project Blog
Kip has a draft of the blog post that will be published on the Open Mainframe Project blog. We need to increase our issues and documentation so someone could grab an item listed in the blog post and work it.

Question if we feel we can meet our goal of becoming an active project by March 15th.
* Ian is close to moving the 3 repos to a Github repo(s) so John can review the code
* Performance Engine - the code is currently in IBM Github and needs over a week of massaging
* A build process is about 50% complete in that it can perform a Git clone to zO/S in USS, and load the zO/S datasets from USS. Remains to build the COBOL, Assembly, and linkedits

Bob think the March 15th data is a bit tight for the Performance Engine. 
CII Badge - we would meet the green, entry level badge. Bob will submit us for the green badge.

Proposal to go ahead and request to be made active by the TAC group by March 15th.
* Discussion around the build process; current build process uses Buildforge which is proprietary. 
* We also need to have some target documentation
* Continuous integration; currently we cannot do this

Should be push out further or get feedback from TAC?
Bob brought up, we need a way to visualize the state of the project. Kanban board, spreadsheet, something. In this way, someone can immediately see the state of the project, what we are working toward, and gaps in getting there. We need to see this ourselves.

Decision was made to push becoming an active project to April
