Meeting notes from the TSC held on October 12th, 2021. 
 
All interested in GenevaERS development are welcome to join.
 
## Conference call details
  
Join Zoom Meeting
 
https://zoom.us/j/98343722378 
Meeting ID: 983 4372 2378
 
### IBM Presentation ###
Kip and Randall will be presenting GenevaERS next week to IBM's open source community

### Misc ###
* Kip fixed the GenevaERS project calendar to reflect that all Tuesday evening (US time) meetings will be held via Zoom
* Kip got pinged by a global financial system
* Kip received an invite to do a podcast on OZE
* Kip's Open Mainframe Project summit video was released on the [Open Mainframe Project's YouTube channel](https://www.youtube.com/watch?v=3neGefGIC1g)
  
#### Documentation ####
* Eugene is translating 600 topics in DITA to markdown. This work could take months to complete. If anyone wants to write documentation, there are gaps in running the performance engine(PE) and optimizing the feature set. Workbench images are out of date and instead the new documentation can utilize text instead of screen shots in many instances
* Kip suggested it may be useful to go through the SAFR museum and update content
* Neil suggested that a good perspective would be the demo; how to run the PE
* Someone suggested having a standing meeting for documentation work. The meetings would be held at 8 PM US CDT
 
#### Workbench ####
* Kip was installing the workbench on his mac. He ran into issues which are unique to his local postgres installation, but it did provided Kip with insights of the user experience
 
### PE ###
* Gillian has been working on a template lookup for direct DB2 reads. SQL would be tailored by the developer. SAFR(commercial version of GenevaERS) is reading DB2 directly in this manner, DB2 manages the parallelism. A use case for using an exit for DB2 reads is when there is a large amount of DB2 data and utilizing the common approach of loading data from the RED files and into memory may under perform when compared to DB2 managing the data access, or when there are memory constraints
* Is there value in putting the template exit in one of the GenevaERS repos?

### R&D ###
* Spark POC - not getting responses from those with deep Spark knowledge that can aid the GenevaERS project with this POC . Work will continue on aspects within their expertise


