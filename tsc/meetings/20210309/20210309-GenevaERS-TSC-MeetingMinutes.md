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

## Blog Post for OMP
OMP published a post on Linkedin referencing our blog entry on the Open Mainframe Project site.

[View the Linkedin post](https://www.linkedin.com/posts/the-open-mainframe-project_openmainframe-genevaers-blog-activity-6773285910390849536-cG0h)

## Issue 103 Mission Statement

As part of the LLC process, we need to come up with a mission / vision statement for the GenevaERS project 

"If you had to explain what the project is and its purpose..."

* We add value in batch processing
* Kip preferred periodic processing to batch processsing
* Removing unneccsary reads to make it faster 
* Flexible, we automatically "rewrite" the systems
* High efficiency

Action Iems is to build up the mission statement over the next few weeks

## Issue 105 Automation for adding a new collaborator

There is a GitHub action which allows people to be added as collaborators to the project.

When someone wants to be added as a collaborator, they create a GitHub issue. Using the following syntax of .invite @Github user name

which allows the automation to pick up the user name and set them up as a contributor to the project

This automation runs everytime a new issue is opened, or an existing issue has a new comment. This is using resources we don't need to use.

A suggestion is to add a label to the issue with the label triggering the automation. However, only existing committers can add labels to issues

It was decided that we would use a combination of .invite and a label to trigger the automation.

## Issue 99 Password Removal

More discussion on this issue has been taking place since the previous TSC meeting.

Michael Shapiro proposed that a script is added to the code for database creation to create an "admin" which would be the person responsible for creation of other user IDs. 

The workbench would validate that the user is a valid workbench user. The password entered is the user's RACF mainframe password.

This approach results in fewer lines of code for Ian to change. 

Machael and Ian have been discussing this and Ian would like to try this approach (Ian was not available for this meeting)

This approach was approved.

Kip placed a summary of the decision in the issue. When Ian is available, he can review the comment and close the issue

## Product Documentation via Gatsby and Markdown

Although Ian was not available to demo his proof of concept documentation site, Andrea got the site working locally following Ian's instructions in the poc's GitHub readme file

Andrea did a screen share so others could see the prototype. There is left pane navigation and on the right of the page is a table of contents for the page. The table of contents is automatically generated off of markdown headings

Next steps are to find out how much of Ian's work is prototype and if Ian would have to make changes to take the documentation site live

Eugene is working on documentation?????????

## Issue 71 Update SAFR Wikipedia Page
There is a SAFR page on Wikipedia. Kip looked into the requirements which now exist for pages on Wikipedia.

The standards have tightened substantally since the page for SAFR went up

The question was, should we create a new GenevaERS page, or update the existing SAFR page to reflect the open source GenevaERS project. Can we do either without triggering the new standards?

## DITA vs Markdown
In order to create documentation in DITA, someone has to learn DITA and tooling.

DITA can cascade a change thoughout  documentation

Learning markdown is much simpler than learning DITA. Since markdown is just text, there are multiple editors one can use to create markdown files

Markdown is more scalable for creating GenevaERS documentation since contributors only need to know markdown and Git. DITA is a disincentive for GenevaERS

Eugene can take DITA content and create markdown files

Eugene guesses only 20% of SAFR is documented and the SAFR workbench documentation is 2 years out of date