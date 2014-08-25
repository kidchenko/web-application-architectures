#Git and Rails

###Distributed Version Control with Git

Git is a popular open source distributed version control system created in 2005 by Linus Torvalds.

Git provides means for comparing the differences between the various versions of a project, and for merging them accordingly.

You should think of these versions as forming a tree
- Main branch is a master
- News versions may be created along the master branch, or new branches can be created off of it
- There branches can possibly be merged back into the master branch

####Git tracks files, which may reside in three "locations"
- Working directory
- Staging area
- Git repository

The files in your working directory can be in one of two  states:
- Tracked: files that were saved to the Git repository by the last commit operation
- Untracked: all other files in your working directory

Finally, tracked files can be either:
- Modified
- Unmodified
- Staged

Commands

- git add . - it takes everything in your working directory and move those files into the staging area
- git commit - if you perform a commit, that puts those files into your local Git repository
- git checkout <branch> - if you want to check out a particular branch
- merge <branch> - if you'd like to merge two branches you issue, Git merge, and the branch name and it, it'll merge that into the current branch
- push <remote> <branch> - you push to the remote repository and you have to specify which branch you'd like to push up to that remote repository
- fetch - retrive a remote repository, you issue the fetch command
- clone <remote> or pull <remote> - is a fetch and it checks out the most recent branch and makes that your master
