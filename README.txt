 Git Cheat Sheet

First `hit`a new repository to work with:
...
$ git init REPO_NAME
$ cd REPO_NAME
...

*NOTE*
Directories are not tracked, just add a `.keep` file

To ignore files add them to `.gitignore`:
...
log/*.log
...

To just add parts to the ind we can use `git add -p`(`-p`as in "patch").

## Disaster Recovery

In case of delete commits use `git reflog`and `git cherry-pick` to recover those commits: 
...
$ git cherry-pick LOST_COMMIT_SHA1
...

**NOTE** Will be cleaned up once `git gc`ran

## Getting information out of history

Use `git log --oneline --graph`to get condensed log view.

Use `git blame` to see **last** change fpr each line.

Use `git show Commit_Sha1`to get detailed information about commit (including diff)

Use `git log -S`to search in contents of commits

## Branches

Branches are essential for any git workflow. To create a new branch run
...

$ git checkout -b BRANCH_NAME

To list all your branches you can run:

$ git branch

Your active branch will be marked with `*`
