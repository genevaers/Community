Meeting notes from the TSC held on May 25th, 2021. 
All interested in GenevaERS development are welcome to join.

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

## Minutes

### Demo Activities
Postgresql database for demo users to see what the demo views look like. Kip's potential solution of using the database that is part of his website hosting solution cannot having public access as it is a shared database for multiple customers.

The Linux Foundation suggested looking for a public cloud solution which could cost GenevaERS money to host. After circling back to the Linux Foundation, it was suggested to reach out to Vicom Infinity. Vicom first suggested a Z solution, which is not what the project needs. In addition, Kip wasn't sure Vicom would want their machine publicly accessible. However, Alex Kim from Vicom suggested an IBM cloud solution. The downside is that the hosting must be renewed every 3 months. There was concern that it would be easy to forget renewal then users would no longer have access to see provided views.

Linux Foundation made another suggestion bitnami which has a low cost public cloud offering including postgres.
AWS has not been explored yet, Andrea thought it would not cost much to host the database on AWS.

Neil continues to work on creating views using the sales data that can be used to highlight the interesting things Geneva can do

Documentation - clarification that documentation needed for the demo release is documentation on how to use the provided demo, not documentation on GenevaERS

Build process - short term the project is working with what we know, which is using JCL. Long term, we do not want to limit ourselves to mainframe tooling.

Sample reference and event files will use the training system files at first, giving them a small set of files. If a user wants to explore Geneva with more data, they can use Neil's data

### Mentorship
Deb attended the TSC meeting and introduced himself. He officially begins June 1st. He will work on coming up with a solution to convert the existing COBOL copybooks for the Virginia data into XML. The XML would then be imported into the workbench 

### Documentation and website updates
The Linux Foundation has created a WordPress instance for GenevaERS. The instance uses the site builder plugin WPBakery which Andrea did explore. Pages and content can use WPBakery or standard WordPress functionality. WPBakery provides templates that can make the GenevaERS site look more modern. We can play around and decide which parts of the site should use WPBakery templates. Also, WPBakery allows users to create their own templates that can be used throughout the site.

Andrea still cannot find where in the admin menu, the theme can be changed.

If anyone with access to the new WordPress instance wants to play around, now would be a good time as the GenevaERS domain is still pointing to Kip's instance

Next steps are to move content from Kip's WordPress instance to the new Linux Foundation provided WordPress instance.

The GenevaERS WordPress instance and domain name registration expire on WordPress.com mid-June. There is a 30 day grace period. Andrea thinks we should be able to move over content from Kip's instance to the Linux Foundation's instance by the renewal date.

### Build Process
With IBM sunsetting Buildforge, on the internal IBM repos, first steps of the build process is to convert to GitHub build process. Additional work will be needed to create two repos; one for SAFR, the other for GenevaERS. The GenevaERS repo would not have the proprietary code such as zIIP enablement. Once completed, the public GenevaERS GitHub for the source code can be created

### Demo video creation
Andrea and Michael have not re-visited. Kip recommended we setup a meeting with Michael next week.
Andrea thought we still had a dependency with the new views being created, but could not recall what that was. Also, Andrea had not received any feedback for the comments she sent back.

### Geneva Documentation
Eugene has created some Powershell scripts to convert existing DITA content to markdown

### Workbench
Jeff is working on correct grammar files to allow import of existing XML

### Performance Engine
Gillian and Neil are working on tidying up messages, roughly 500 messages.

### Spark POC
Not much new activity. We can handle IO, call assembler from java and think we should be able to call java from assembler

## Reminder, the US is on holiday next Monday
