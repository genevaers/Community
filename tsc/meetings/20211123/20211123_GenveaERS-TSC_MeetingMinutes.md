
# Meeting notes TSC November 23, 2021
(in USA, in Australia Nov 24).

All interested in GenevaERS development are welcome to join.

## Conference call details

### Zoom Meeting

https://zoom.us/j/2181293577 Meeting ID: 218 129 3577  

## General Updates 

We got a nice plug from John Mertic on the "I Am a Mainframer" podcast.
1 or 2 week podcast.  
[Link](https://www.openmainframeproject.org/blog/2021/11/23/i-am-a-mainframer-john-mertic)

Steven Dickens interviewed John Mertic.  Mentioned GenevaERS and Open Mainframe systems in general.

## Article in Enterprise System Journal

Journal is at ESJ.com.
Kip to write article by December 3. 
Friday meeting will discuss content:
- GenevaERS
- Open systems on Mainframe
- "In situ" data analytics
- Business benefits

Sandy suggested that GenevaERS is best for "heaving lifting" or data.
Spark needs to be in section on Python and language called "R".  
Contents suggestion will be emailed to ask for review.

## Website Updates

Andrea unable to attend - no update.

## Ian Cunningham update on Workbench

Continuing to work on COBOL Copybook converter.
See GitHub GenevaERS wb repo.
Issue #22 COBOL Copybook Converter shows items done and items "to do".
Will need to rename assest listed Relaases, Assets.
GenevaERS.zip is MAC version.
release.zip is Windows version.
First real release will be 4.50.

Ian feels the workbench area needs proper project management.
1.  Ian to create Project at GenevaERS level.  Allows issues to be anywhere if spinoff issues arise.
2.  Reviewers for Ian changes.  Gillian Hannington volunteered.  Michael Shapiro may also be interested in doing this.
3.  Prepare milestones for 4.50 Release.
4.  Ian will prepare documentation on how to download binary and run (no need to build).  Works for both Windows and Mac.

REDEFINES to come.
VALUE clause in COBOl not relevant to record layout.
COMP, PACKED already supported.
Decimal point not yet.

## Gillian Hannington and Neil Beesley update on Performance Engine

Pipe to Python can be done with Hypersockets using TCPIP.  It is really done with a Cross Memrory Services call. 
Sandy suggested GenevaERS is best used to prepare for analytics.
GenevaERS is not really an analytical package.
Python has libraries of analytics procedures.
Bob said GenevaERS is more an ETL (Extract Transform & Load) product.

Gillian said Lookups being tested with Hash Tables.  Had adhievced 17% improvement even with collisions.  Will test further.
Good results with key packed into 16 bytes or less.  Neil to help.

##  Eugene Morrow update on documentation.

Eugene shared his screen showing a new website for GenevaERS General Documentation.  This new site uses Gatsby technology. The top line clearly shows "UNDER CONSTRUCTION".

Eugene showed the screen structure:
- Left side has a table of contents of all topics (expandable)
- Middle show the current topic and has links to other topics
- Right side has a way to jump between headings in one topic.

Home screen show a list of folders of topics:
01 and 02 are for people new to GenevaERS.
10 to 99 are for people more familiare with the site so they can get to resources quickly.

Website has bug: last topic in each folder crashes the site (except for the last topic in the last folder), so as a workaround Eugene created topics **ZLastDummyLast01.md** in each folder to allow the other topics to display properly.  Do not click on this topic if you see it.  Ian offerred to help Eugene find a JavaScript solution.

In the next week Eugene will put up on GitHub Pages so everyone can see and udpate the website without having to have Gatsby on their laptop.

This will work like other parts of the GenevaERS project: people can create a branch, update something, and create a Pull Request.  Others can review and Merge the PulL Request.  Issues and milestones and releases as for other repos.

Next Meeting: December 14, 2021 (USA) 
              December 15, 2021 (Aust)
