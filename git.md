GIT
==============

| Commands | Reason | 
| --- | --- |
| git add . | Add all new files to be commited | 
| git add -u | Record changes to all files like deletions |
| git commit -m "commit message" | Commit all recorded changed |
| git push | Push files to remote |
| git fetch | Check for changes on remote |
| git pull | Pull in remote changes to current branch |
| git checkout -b feat/branch origin/feat/branch | Checkout remote branch with upstream |

## Branches

Create new branch: **git checkout -b feature/<new_branch>** 

Push to remote: **git push --progress --porcelain origin refs/heads/feature/<new_branch>:feature/<new_branch> --set-upstream**

Check out remote: **git checkout develop**

Delete remote and local: **git push origin :feature/<branch>** and **git branch -d feature/<branch>**
