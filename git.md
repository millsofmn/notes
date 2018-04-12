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

## Branches

Create new branch: **checkout -b feature/<new_branch>** 

Push to remote: **push --progress --porcelain origin refs/heads/feature/<new_branch>:feature/<new_branch> --set-upstream**
