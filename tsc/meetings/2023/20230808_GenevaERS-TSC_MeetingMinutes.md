# Meeting notes TSC 2023-08-08 6pm Pacific Time (US)
All interested in GenevaERS development are welcome to join.
## Conference call details
### Zoom Meeting
https://zoom-lfx.platform.linuxfoundation.org/meeting/95522057563?password=a2cb4656-98bd-4f6e-9d48-2998457acf72
## Attendees 
- Andrea Orth
- Bob McCormack
- Gillian Hannington 
- Ian Cunningham 
- Kip Twitchell 
- Michael Shapiro 
- Neil Beesley 
- Randall Ness
## Administration
- The description of what GenevaERS could be improved on https://genevaers.com
  - Option 1
    - What is GenevaERS? 
      - Open-source software for use in the IBM z/OS mainframe environment
      - Generates highly efficient machine code for tremendous scalability
      - Can be an ETL (Extract Transform and Load) tool but for reporting and extract processes
      - Or can be an application-development engine
      - Created for reporting processes for the world’s largest financial organizations
    - What is it Not?
      - A database or database-centric technology
      - An end-user query tool
    - What does it do? 
      - Rapidly produce many outputs in one “pass” through a data store
    - Why is it important?
      - Allows data analysis:
        - At very low levels of detail, and of many more attributes and various coding structures including legacy and transitional code blocks
        - With greater history
        - To support many more financial, regulatory, management and even risk analysis outputs
      - Which all reconcile, are consistent and have the same cutoff
    - What are the business benefits?
      - Reconcile source data prior to discovering issues in production
      - Shorter closing cycles for reporting 
      - Great transparency
      - No charge for software use
      - Reduced financial system inventory
  - Option 2
    - GenevaERS: 
      - Provides a business-reporting solution for z/OS, uniquely tuned for high-volume data scanning
      - Delivers a foundation for improved financial transparency and better decision-making
      - Mitigates audit and reconciliation concerns by tightly integrating reporting with the source data
      - Leverages existing investments in mainframe technology and reduces operating costs
- GenevaERS annual review at the OMP TAC meeting 
  - The following repos in have been published in the GenevaERS organization in the public GitHub
    - Performance-Engine 
    - Performance-Engine-R-and-D
    - Run-Control-Apps
    - Workbench
  - We now have a committer who is not associated with IBM or an IBM client
## Infrastructure
- Developers must have installed the  Developer Certificate of Origin (DCO) app. 
  - https://github.com/apps/dco
- Overview of branch protection rules 
    - Pull requests are required.   
    - At least one approval is required for pull requests.  
      - Should we remove the requirement for reviews on repos with source code? 
        - This would allow developers to move more quickly. 
        - If we as a team didn't like the change, we could remove it after the fact. 
    - Verified signatures are NOT required. 
    - Administrators cannot override the rules. 
  - 2FA now mandatory on GitHub 
    - https://github.blog/2023-03-09-raising-the-bar-for-software-security-github-2fa-begins-march-13/
  
## Run-Control Apps
## Workbench
  - When you view HTML reports with a web browser, you don't have a horizontal scroll bar 
    - **Try workaround of saving the HTML file as a PDF.**
  - How does the Compare Utility work? 
    - Does it run the Dependency Checker behind the scenes?  **No.**
      - How does it deal with inactive components? 
    - **Don't make any changes for now.**
    - **Mention that some components may not be compared in the documentation because the view is in inactive status.**  
## Performance Engine
## Potential users (who may want support)
## Demo
## Documentation
- "A document a week, that's all we ask" 
## R&D Work
## Conferences 
- Possible presentation at the Winter SHARE conference 
## For next time 
