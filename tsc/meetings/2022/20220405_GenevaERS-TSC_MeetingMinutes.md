
# Meeting notes TSC April 4, 2022 (US)

All interested in GenevaERS development are welcome to join.

## Conference call details

### Zoom Meeting

https://zoom.us/j/2181293577 Meeting ID: 218 129 3577  

## Mentee Discussion 
Mentor program for this summer is starting up. We don't know yet if we will get a mentee. Discussion continued around a previous idea from this past [January](https://github.com/StateFarmIns/community/blob/master/tsc/meetings/2022/2022Jan11_GenveaERS-TSC_MeetingMinutes.md) for using Zowe to take the XML from the workbench, upload to the mainframe and kick off the performance engine

Ian noted that Zowe wants to be part of the discussion around this possible work

Also, Ian has been looking at another way to manage the framework. We would need to capture what we want the outcomes to be of this work.

Kip thinks the mentee would be assigned in May. We need to document what we want the mentee to work on

## Demo
The previous R&D meeting reviewed the performance engine demo and felt pretty good about it. Documentation for the performance engine demo was updated after the demo

We now need to circle back to the workbench demo. We need to determine what we would give them to help them understand Geneva using the demo views.

Kip threw out a goal of scaling up the workbench demo during 2nd quarter

## When someone comes into Geneva org, what do they see?
This discussions touched on GenevaERS.org and GitHub
On GenevaERS, Andrea will add a link to the new PE documentation. She also mentioned how she was thinking of adding something to the site similar to linktree style "one stop shop" formats

Kip's question is referencing the [GitHub organization](https://github.com/genevaers)
- Question - can we have a Readme at the org level? No
- Question - where does someone start if they start at GitHub? Gillian thought someone would start at the doc repo. We could update the Readme at Community to point people to the doc repo or whatever repo makes sense
- Andrea looked at Zowe's GitHub organization page and they have "pinned" repos 

What's next for this?
- Maybe the Readme sends people to the static site, GenevaERS.org. We could also update the Community Readme

## Documentation
"A document a week, that's all we ask" 

### Where do we start?
Gillian would like a discussion. Kip countered with encouraging something simple which would help us come up with additional documents which could give an overview of Geneva

### New syntax docs
Randall did a demo of the new syntax markdown documents which were created by using the old Word syntax files. When using the Word docs, there was no versioning other than making copies of the syntax documents.

Randall is pleased with the new markdown documents. Git / GitHub allows for easier versioning than the old method of having multiples copies of a document

Randall is also making specs for our output reports and says they also should be in markdown.

Randall's documents are in the MarkdownTest repo and website.
See MR91 examples
- [GitHub MR91 syntax](https://github.com/genevaers/MarkdownTest/blob/main/docs/GVBMR91_Parameter_File_Syntax.md)
- [Website MR19 syntax](https://genevaers.github.io/MarkdownTest/GVBMR91_Parameter_File_Syntax.html)

## Workbench
Ian has been looking at the [Eclipse Modeling Framework](https://www.eclipse.org/modeling/emf/) (EMF). He thinks this is something that can be used for the workbench. It would require a different approach that what is currently used to build the workbench.

Ian showed the [Eclipse Epsilon](https://www.eclipse.org/epsilon/) website. Epsilon has tools for graphical editors. No database is required. Code can be created and edited graphically. Ian thinks Epsilon is worth investigating

## Performance Engine
Gillian and Neil are working on RTC 22618. They know what they are working on will work, but want a universal solution. Gillian also continuing to work on the >256 LR field issue

Question - what would it take to use zLinux?
- When we return to zLinux, we can use knowledge picked up when working on the I/O work

## R&D Work
- Consider a calendar and e-mail list for the group

Andrea will run the next Tuesday's international R&D session and the next TSC meeting
