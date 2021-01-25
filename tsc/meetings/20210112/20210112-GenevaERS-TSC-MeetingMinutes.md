#### Open Mainframe Project mainframe committee
We proposed to the Open Mainframe Project(OMP) a workgroup, which is being run by members of the GenevaERS project. The workgroup is discussing Public z/OS cloud enablement. Met last month with the Technical Advisory Committee (TAC) the feedback was pretty positive. The workgroup had their first meeting before Christmas and the 2nd meeting last Thursday discussion how OMP can enable z/OS public cloud to overcome problem the GenevaERS project has been having with our project.

For anyone that wants to donate Z resource, how can we make it easier to make contribute? It may include some system scripts to lesson the burden on a donatee's system programmers.

Sample dimensions
* Tenancy - multi tenant vs. single tenant
* Hardware - donated hardware vs owned hardware
* Emulator - bare meta, zD&T, & zPDT, zVM
* Interactions - interactive development, CI/CD
* User organization type - community, single company, multi company
* Sysprog support model - shared, independent, semi-independent (sysprog for dependent environment)
* Cost - charged (fixed, usage based), free
* Processes - Transaction and service hosting, analytical
* Load - number of users, resource contribution model
* Contributing organization, academic, commercial, others

#### Progress to date
* 6 months ago, we became an incubation project
* We have a GenevaERS website and a YouTube channel
* Active community with roughly a half a dozen non-IBM developers contributing to the project
* With the assistance of Vicom Infinity, established a mainframe working environment for the project
* Removal of proprietary software components from GenevaERS
* Defined architectural direction
* Significant contributions to the OMP through videos, the public zO/S workgroup leadership, podcasts and webinar contributions

Kips "I am a Mainframer" podcast will be released this month

#### Spark integration
Neil, Randall, Sandy, and Kip had a 2 hour R&D session and removed again Neil's work on success jni calling assembler. Performed a simple call from java through the C++ language environment to get to assembler. C does the conversion from ASCII to EBCDIC and back.

Proves we call UR20 and maybe have communication between SAFR and Spark.

Met today with the IBM offering manager and technical manager for IzODA. Kip outlined GenevaERS work with Spark. We were given access today to use the latest version of Spark on an internal IBM machine.

#### Marketing
* Last year Kip began working on a Geneva in one minute video. Kip has a script and Sandy, Andrea, and Geneva have been trying to figure out how to compliment what Kip is describing.
* Maemalynn sent an email and asked about our GenevaERS blog post. They want to run the blog post on the OMP site with our plans for next year.

#### Mentorship Ideas
OMP has a mainframe mentorship program. They are looking for suggested mentorship tasks that a group of college students could work on. Do we have things they can work on to enhance the understanding of the mainframe and open source projects?

* The zowe explorer cannot display data in hex and understand mainframe record formats like ISPF does. We want to see the record formats on the mainframe. Ian raised an issue,#1135, on the zowe explorer github site. This idea is more of a zowe idea, not GenevaERS as Vicom does not have zowe.

* Ian - has been generating descriptions of VDP and logic table record formats. Ian was going to get Jeff to learn a bit of java and produce some documentation in html format. By understanding the formats of these records, they would exposed to some mainframe concepts. We need to document this process.

* Maybe some documentation of our current processes they could do? But there is a big problem with SAFR in that it is complicated for new people to pick up.

Action item is to open an issue so people can use to populate with ideas.

#### Performance Engine
* Gillian - spent some time documenting XRCK. The zIIP code changed last year has been tested and thrown some issues that need to be looked into.
* Kip - we'd like to get out of project incubation stage by March and be a formal project. In order to do this, source code releases are something we need to be working on in the next couple of months. Relative to the PE, we need to finish testing the separation of the zIIP code. There's a DB2 model that needs separating out. We need to decide which exits we are going to include. We also need to determine how we will manage the code. Kip told John we want to be put on the TAC's March 12th agenda.
* Neil was looking into issues about pipes and what we need to do is create an error message.

#### Infrastructure
* Bob - we've created an rtc stream which will be deliverable for the workbench that is deployed in the open source world. Then deployed Apache rat against it which will automatically provide the Apache 2.0 copyright notice in the files.
* Static scans were run against the rtc and a minor issues were found regarding licenses. These will be fixed shortly.
* The macros in our source code are available via PTF. Customers who want to use these GenevaERS ptfs will have to have the assembler toolkit, which is a priced product. 
* One of the data files on the Vicom machine has been modified to have packed decimal and not just numeric format.

#### Misc
* We now have organizational authority to add new committers to the GenevaERS community repository. This came about as part of a discussion with John, Kip, Sandy, and Andrea
* The current github committers agreed to add Bob as someone with organizational authority, which means he can create repos.

