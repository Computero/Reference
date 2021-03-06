# GitHub Command CheatSheet

### Create a new local repository
From inside the directory you want to use for the repo

`git init`

### Check out a repository
`git clone username@host:/path/to/repository`

### Add files
###### Add one or more files to staging
`git add <filename>`

or

`git add *`

### Commit Changes
`git commit -am "Commit message"`

### Push
Send changes to the master branch of your remote repository

`git push origin master`

### Status
List changes you still need to add or commit

`git status`

## Working with Branches
###### Create a new branch and switch to it
`git checkout -b <branchname>`

###### Switch from one branch to another
`git checkout <branchname>`

###### List all the branches in your repo
`git branch`

###### Delete the feature branch
`git branch -d <branchname>`

###### Push the branch to your remote repository
`git push origin <branchname>`
