Attendance
Andrea Orth
Bob McCormack 
Randall Ness 
Sandy Peresie 
Ian Cunningham 
Jim Hladyshewsky 
Gillian Hannington
Neil Beesley

Performance Engine
Continuing with handover / knowledge transfer from SAFR team retirement.  Currently fixing problems found in code.    Only difference in code base between SAFR and Geneva is that zIIP will unavailable with Geneva.  All Geneva source code will need to be moved to GitHub.  Process and procedures need to be finalized for updating code in that environment.

Workbench
Database should be set up in the next week or so.  Not much progress but a few issues were found.  
Applying some fixes from SAFR version.  Ian is working on a Java equivalent of MR91.  Workbench code will go under GenevaERS.

Infrastructure
CIO Badge reminders will be sent until it is complete.  We are at 6 months and have a year to complete.  SAST (security test software) is needed for the badge - will use Visual Studio to edit Git Source.  Looking at Checkmarz and KlocWork Veracode.  DAST - dynamic app secuity test - we need to consider the workbench running on Windows or Linux.  
Have the ability to perform builds on the Viacom machine.
The State of Virginia data had a value that was not compatible with high level languages.  Converted mathematical data to packed decimal.
Need to deploy scan software for licenses and are looking at ToolKit.
Need to ensure the storage of passwords in the workbench need to be handled by an appropriate security product.
For moving PE source code out of IBM, there be a repro on the IBM side and then verify that all the parts that need to be there and those that shouldn't be there are removed.

Viacom
ID issues have been resolved on the Viacom machine.
New Linux environment being set up with Postgres.
Randall has set up some test JCL.

Issues
#78 - Looking at products for issue tracking / boards
?? - John still looking for ways to get people added to the project
