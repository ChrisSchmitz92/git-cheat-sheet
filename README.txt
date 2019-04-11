
#Git Cheat sheet

First 'init' a new repository in work with:

$ git init Repo_Name
$ cd Repo_Name


**Note** Direcotries are not tracked, just add a '.keep' file

To ignore files add them to '.gitignore'
...
log/*.log



to just add parts to the index we can use 'git add -p' ('p' as in "patch")

## Disaster Recovery

In case of delete commits use 'git reflog' and 'git cherry-pick' to recover those commits:
...
$ git cherry-pick Lost_COMMIT_SHA1
...

**Note** Will be cleaned up once 'git gc' ran
