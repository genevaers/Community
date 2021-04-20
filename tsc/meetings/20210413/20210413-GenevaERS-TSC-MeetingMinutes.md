Meeting notes from the TSC held on April 13rd, 2021. All interested in GenevaERS development are welcome to join.

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

## Minutes

### Git Workflow
Ian said we need to choose our workflow.
Main choice is between forking and branching.

Forking creates an entire clone of the repo.  Sandy confirmed forking does update JIRA.
There is a link to a BitBucket site that explains the differences in workflow.  Once on that site, click on [“comparing workflows”](https://www.atlassian.com/git/tutorials/comparing-workflows) at left.  People need to read this.

Note that JIRA has its own workflow that is separate from Git.

BitBucket does the same job as GitHub.  BitBucket is the Atlassian equivalent of GitHub and is better linked to JIRA.  There are not BitBucket issues – only JIRA issues.  However we are too far down the track to change from GitHub, and it has lesser links to JIRA.

**Consensus:** 
* Never work on the Master.
* Internally in the GenevaERS project, we will use feature branch workflow.  Branches are easier than forks which need to maintain the fork with changes to the master.  There is also less storage used for Branches as compared to forks.
* GenevaERS will name the branch “GDIssue-initials-feature”.  The software converts blanks to a dash automatically.  Example: “GD-25-IC-initSiteGenerator”.
* There is always a reason for Branch: either feature or bugfix.  Create a JIRA Issue so that the Branch has that GDIssue in the name.
* Companies outside this project that create something for their own use should use a fork.  This needs to be included in “How we work” documentation. (Andrea.)
* Anyone outside this project who wants to contribute needs to use a branch.  This needs to be included in “How we work” documentation.  (Andrea.)
* In GenevaERS project, we create a branch, work on it, create a pull request, and then delete the branch.  

### Documentation GD-98
Ian said we will use Gatsby.  He will create a Pull Request to pull in his changes very soon.
He has a few things to cleanup.  Also need to look at fonts, colors and so on.

Need to clarify license for Gatsby template – a third party license.

There are lots of issues with documentation.  Gillian said she wrote some notes in JIRA on this.

Big issue – testing GenevaERS.  Need documentation on how to download, install and run a minimum number of test cases.  

We start with something and build on it.
Randall as some training data for this called the “green sock” database..  See these datasets at Vicom:
GENEVA0.TRAINING.JCL.  Example member: INTRAINC1
GENEVA0.TRAINING.WB.XML
GENEVA0.TRN.*    Training files of data.

There are some small view that run say 10 to 20 records.

The full test suite we currently use for SAFR is too big and confusing to use.
Need visibility of what we are testing and how it works.

Randall remembers some data that had 50 states and sales covering last year and current year.

May need to automate creating orders data using IBM tool IEBDG (Data Generator)
Randall to create an issue in JIRA for this.

Andrea left meeting due to network issues.  Sandy took the chair role.

### Java MR91
Ian is close to creating a minimal process of a Java MR91 that can pick up some simple records and pass to the Performance Engine.

This provides a pipe between a user at a laptop creating simple XLT and VDP files to run in the Performance Engine.  Currently very limited.

Need to list the features that need to be added and what order they can done in.  Ian and Jeff Horner will program.

Guide can be Randall’s views from the “green sock” database.  

Importing views into the workbench not yet prepared.
Once we can import Randall’s views we can build on that, and use that as guide to the priority of extending MR91.

Randall nominates View 16 in Environment 4 of SAFRWBTR schema.

### Issue GD 117  Update Committer CSV
Issue closed.

Next meeting April 27 (USA) = April 28 (Aust)
