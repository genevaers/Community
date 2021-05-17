Meeting notes from the TSC held on May 11th, 2021. 
All interested in GenevaERS development are welcome to join.

## Conference call details

Join Zoom Meeting
https://zoom.us/j/94966206199

Meeting ID: 949 6620 6199

Participants
* Kip
* Ian
* Bob
* Jeff
* Sandy
* Randall
* VenkateswaraKaikala
* Gillian

## Minutes

### Website Transfer Update
The domain name ownership has been transferred to the Linux Foundation. The latest update indicated the WordPress instance under the Linux Foundation should have been provisioned yesterday, but no confirmation yet from John

The domain name for Genevaers.org needs to be renewed; the expiry date is June 17th

### Build Process Update
Bob and Randall are working on tasks in parallel. 

### JIRA vs GitHub

JIRA allows for Epics, Stories, Tasks

Benefits of GitHub management
* Everything is in one place; code, issues, etc
* Public
* Easier for a contributor to create issues in GitHub than JIRA

GitHub Kanban boards can exist at the GenevaERS level which spans multiple repos. Boards at the GenevaERS level can be thought of as epics. 
Kanban boards can also exist at the repo level.

Using labels, it is easy to filter a Kanban board by clicking on the label

GitHub Milestones can be thought of as stories (or Features for people familiar with other tooling), items on a Kanban board are grouped under a Milestone. There is a progress bar that displays completion of the work aligned with the Milestone

There does not appear to be a way to put a date on the Milestones

Sandy has already begun setting up items from issue #125 - demo in a Kanban board

Members on the TSC call approved shifting from JIRA to GitHub project management

Action Items
* The demo work should be the use case for GitHub project management. Kip would like to see us populate the demo Kanban in the next 2 weeks
* We need to define our workflow so when new issues come in from a future contributor, a committer reviews it and assigns the issue to the appropriate Kanban board. Only committers can do the Kanban board assignment

### Mentorship Update
The mentee does not know the mainframe but is interested in learning. He selected a 6 month mentorship and has until May 15th to formally accept the mentorship offer

He will work on allowing the Virginia data to be used

He lives in India, not the US

### Demo Progress, Issue #125
To run the demo, someone interested in Geneva does not need all of the components of Geneva such as the workbench and the postgres database. They are provided a set of JCL that runs all of the views in one pass
We do want to note that a view is an independent thing

Who is the target audience for the demo video? Someone new to the mainframe like the mentee or someone from an organization that has business needs satisfied by running workloads on the mainframe?

### Shared environment
We need to manage our metadata like source code. What does this mean for a shared environment?

We could use Kip's website host and create a postgres database that can be populated with metadata. People interested in Geneva can see the metadata. Updates, new metadata would be restricted to a few people
