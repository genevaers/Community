
# Meeting notes TSC March 22, 2022 (US)

All interested in GenevaERS development are welcome to join.

## Conference call details

### Zoom Meeting

https://zoom.us/j/2181293577 Meeting ID: 218 129 3577  

## General Updates 
Can we make a different email list for the R&D meeting schedule? Would a subgroup give us what we need?

Kip could ask during the next TAC what zowe uses for their calendar and email list

## Website Updates
- New Repo Needed for website administration documentation
Kip created the new private repo,WebConfig, during the meeting. Andrea and Kip are the committers. This repo will hold website configuration information

## Demo System Status
- Docker Instance Progress
Putting the workbench in Docker is easier if the workbench is empty. We can have an empty workbench and have demo XML available for importing the metadata and views into the workbench

- PE Documentation Progress (What the demo does)
Michael made some suggestions regarding the demo system, some of his suggestions were incorporated, but not all can be done at this time

### Who is our audience for the workbench demo?
- How do we build off of the PE demo?
A user would make changes in the workbench and run PE to see the results.

We need to think on the use cases for the workbench demo. What would be the core concepts that we want an inexperienced person to learn? Kip suggested this could be the topic in next Tuesday's international meeting.

## Documentation
- Test Repo for Jekyll
Eugene created a new repo, [MarkdownTest](https://github.com/genevaers/MarkdownTest), where people can code a GenevaERS topic page and see how the text and images render in Jekyll

Follow the directions in the Sample.md file

Eugene noted that links and images work differently between jekyll and gatsby, but Eugene thinks he can automate moving content from this jekyll powered site to the gatsby powered site. A good goal would have one document a week created in the MarkdownTest site

## New Build Process Progress
Bob is working on local and open source builds. In the future, his work will be merged with Randall's build process

## Workbench
Ian is trying to extend the workbench to run control analyzer. 

We need to think about licensing to think about licensing for DB2.

Similar to PE, we don't want to perform dual maintenance on an open source version of the workbench and non-open source version 

## Performance Engine
Working with Neil on his I/O improvement work. Hashing work is ready, but would need to be added to the build. Both are looking forward to Randall's new build process

## R&D Work
- Meeting moved to 1 PM ET
- Consider a calendar and e-mail list for the group

## Issue Review
Regarding a security issue auto flagged by GitHub, currently a private key is not being used, just a code statement. Bob remarked when the fix is committed, the scan will automatically run again
