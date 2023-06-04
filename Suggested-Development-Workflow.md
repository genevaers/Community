# Suggested Development Workflow  
  
1. Start with the remote main (or master) branch.  
1. If the repo is not on your local drive, clone the repo to your local drive.  Otherwise, do a `git pull` to the local drive. 
1. Create a local development branch.  
1. Repeat until you are done with your change: 
    1. Repeat until you are done for your current session: 
        - Make your changes to the source code.  
        - Loop.  
    2. Publish your development branch. (It’s good to have an offsite backup).      
    3. Loop.  
2. Make sure your local main branch is in sync with the remote main branch.  
    - If not, `git pull main`, then merge to the development branch and publish again.  
3. Create a pull request on remote.  
4. Merge the pull request on remote.  
5. When you are finished with a branch: 
    1. Delete the development branch on remote. 
    2. On local (using either the Git command line or VS Code):
        1. `git checkout main`
            - To point to the local main branch.
        2. `git pull` 
            - To get local main branch in sync with remote main branch. 
        3. `git branch -d <branch-name>`
            - To delete the development branch.
        4. `git fetch –-prune`
            - To delete the remote tracking reference.
