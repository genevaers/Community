Meeting notes from the TSC held on July 13th, 2021. 
 
All interested in GenevaERS development are welcome to join.
 
## Conference call details
 
Join Zoom Meeting
 
https://zoom.us/j/94966206199
 
Meeting ID: 949 6620 6199
 
### One Year Review ###
Next month, at the Open Mainframe Project's (OMP) Technical Advisory Committee (TAC) meeting, the GenevaERS project's incubation status will be reviewed. Status will either remain incubation or the project will be elevated to Active.
 
### Demo progress 
 
#### Performance Engine pre-process 
Ian
* Getting closer to taking the XML files and can almost generate the jlt files. Hopes to finish that work in a week.
* Estimate is 3 weeks to take workbench XML and generating the jlt & xlt file in the java codebase. Won't have the current state reports but it will function
 
####  Performance Engine ####
* Randall is documenting which modules are in GenevaERS and which modules are exclusive to SAFR
* Gillian is tidying up error messages
* Neil is working to make reports consistent on the extract reports
 
#### Build process updates ####
* Bob and Randall working on the build process to have an easy way to download and upload to a mainframe
* Randall has been working on documentation for the instructions and will update the README.md file in the GitHub demo repo
* Randall has been researching GitHub's release functionality and all of the demo components will use the same tag
* Until there is a complete build process, the demo will be providing a load library which is being created by IBM's internal SAFR process
 
#### Workbench ####
Jeff
* Working on vulnerabilities
* All of the postgres scripts work
* Users can take the provided views and run the performance engine using the short term process of utilizing MR91. Longterm, a java based MR91 will replace short term MR91
* Users can also import the views into the workbench, export them and run them through the performance engine.
 
#### Sample Views ####
Key features of the demo views
* Simple extract
* Extract with multi-step join
* View that writes to a token and in subsequent views does effective dated lookups, aggregation, and summarization
 
#### Video for the demo ####
* Michael has been working on a script for the first video for the demo
* Goal is to generate enough interest that they will download the demo
* We want to use short, concise words to express GenevaERS concepts performed by the demo views
* We may have a video for each that explains what each view does
* Bob has something that will generate pictures Michael can use in the video(s) he's working on
 
#### JCL to run the views ####
* Only need one version of JCL for upload, install
* Each pass has it's own job
 
#### Documentation for the demo ####
* Gatsby will be used for rendering the documentation in the markdown files
* By end of the next week, Bob and Eugene will try to have something that the team can contribute to
* Instructions for ftp to a mainframe will be provided. The documentation will be based on the user having a windows machine
 
#### Misc ####
* Who is the audience for the demo system - non-mainframers who have problems to be solved
* Kip and Randall are creating a proposal for the 2021 Open Mainframe Summit
 