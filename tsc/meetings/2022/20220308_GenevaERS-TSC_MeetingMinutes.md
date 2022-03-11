
# Meeting notes TSC March 8, 2022 (US)

All interested in GenevaERS development are welcome to join.

## Conference call details

### Zoom Meeting

https://zoom.us/j/2181293577 Meeting ID: 218 129 3577  

## General Updates 

### Badge Offering
We can issue badges to project committers. Everyone who is a committer will receive a badge. The badge offering will come via email. Before the meeting, Kip did some cleanup on the committers.csv file. The group discussed additional changes regarding committers on the different repositories the project uses. Kip will update the csv file.

Question during the discussion - will there be a separation of content between the test framework repository and the test cases the framework will run?
Answer - we'll discuss when we're closer releasing the repo

## Website Updates
The website is working again. A note will be taken to the next TAC meeting regarding clarity in the ticket status updates.
A blog post was published to send people to the article Kip and Randall wrote for Enterprise Systems Journal.

## Demo System Status
During last Friday's R&D session, revisited documentation. Work will continue this Friday.
Documentation needs updating to better explain what the demo does

Michael was sent a link with some work to do regarding lookups. Michael is trying to install the latest demo but running into some difficulty which he and Ian will work on.

Workbench demo - Docker will be used to "package" the PostgreSQL database. The workbench can be added.

IBM's cloud came up as part of the demo discussion. IBM's cloud does offer PostgreSQL and Docker. Ian sent Kip an email about this.

## Documentation
We need to have some supporting images in the documentation that can explain the relationship between the data going in and the multiple outputs being produced. Michael will work on this

What documentation work can be done while Eugene works on the Gatsby powered documentation site?
This site will be used for the type of content contained in the earlier "Balancing Act" documentation. People can begin creating topic in markdown. This work is de-coupled from the "backend" Gatsby work

Difference between Gatsby powered site and Jekyll powered site.
With Jekyll, markdown content updates automatically get pushed to the site by the site.
With Gatsby, there's a markdown commit and a second "commit" to get an update published

Maybe there would be value in creating a second Jekyll site for community updates to documents

## Mew Build Process Progress
Work continues on the new build process. Randall, Bob, and Gill will work on some issues after the TSC meeting. 
For some modules, Randall would like to maintain a single code base between SAFR and GenevaERS.

## Performance Engine
Last week, Gill and Neil discussed a design for improving I/O.
Working with Ian to generate common data areas

## R&D Work
Continues to be focused on the demo system
