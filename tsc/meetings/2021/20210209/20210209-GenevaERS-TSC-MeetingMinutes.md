Meeting notes from the TSC held on February 9th, 2021. All interested in GenevaERS development are welcome to join.

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

## Attendance
* Randall Ness
* Gillian Hannington
* Ian Cunningham
* Eugene Morrow
* Bob McCormack
* Kip Twitchell
* Andrea Orth
* Sandy Peresie
* Venkateswara Kaikala
 
# Minutes

## GenevaERS, our influence, and becoming an active project
A large portion of the meeting had discussion items that revolved around the larger GenevaERS project. 

Linux Foundation is very complimentary to our project. Our project's influence is more broad than just GenevaERS. Based on difficulties and issues GenevaERS has encountered seeded the Open zOS Enablement working group(OZE).

Regarding OZE, the working group has two leads on possible code contributions.
Another item to note from that discussion is [this blog post on running Z on AWS](https://aws.amazon.com/blogs/apn/deploying-ibm-mainframe-z-os-on-aws-with-ibm-zd-and-t/)

Back to GenevaERS. The project has a goal of moving from incubation project to active project before the 25th which is the 25th anniversary of "the death of the mainframe". The project hopes to go to TAC on the 11th of March to get approval for becoming an active project.

What is necessary for meeting the badge requirements?
* The workbench code does not meet the requirements for passwords and database credentials
* Outside of the credentials issue, the rest is just created operating procedures (OP) for scans, versioning, etc...
* We need three repos created for Ian's workbench code, test framework code, and the java fronted
* the 3rd party document needs to be updated

Options for having something people could download and use to meet the active project requirements
* Release the performance engine (PE) code. We could provide VDPs and people could take the PE and VDPs and run them on their mainframe
* Release Ian's testing framework which does exercise the PE through FTP

## LLC
The Linux Foundation creates a LLC for projects to protect the intellectual property(IP) for each project. The owning entity of the assets of GenevaERS will be owned by a LLC the Linux Foundation will create.

## Blog post for Open Mainframe Project Blog
GitHub Issue #92

We need to being drafting the blog entry that announces GenevaERS becoming an active project by March 15th.

## Website options
Currently the GenevaERS.org website is using and is hosted by WordPress. Is WordPress the long-term strategic direction for the GenevaERS website?

Discussion point:
* We want to use a tool that does not hinder us
* We do not need to make a tooling change before the 3-15 anniversary date
* Bob has been looking at Gatsby and Eugene has been involved
* Zowe's website and documentation site is using vuepress and has found it limiting

## Data discussion
Question was asked, should there be a cutdown of data placed in GitHub?

Discussion noted that the data we've been using on our mainframe instance has had to be "massaged" to better reflect the type of data used on the mainframe. Could this type of work be something a Open Mainframe Project mentee could do? It was not known, if the submission period was still open.

