# Basic git commands

### Explaining the workflow

Working directory to staging area : `git add`</br>
Staging area to local repo : `git commit`</br>
Local repo to remote repo : `git push`</br>
Remote repo to local repo : `git pull`</br>

### Commands
```
git --version
git init
git add <filename>
git add -A
git status
git commit -m "<commit_message>"
git commit -a -m "<commit_message>"
git remote add origin "<html_link>"
git remote add origin "<ssh_link>"
git pull origin master
git push origin master
git push origin <branch_name>
git log
git branch <branch_name>
git checkout <branch_name>
git checkout master
git checkout <first_eight_hexa> <file_name>
git merge <branch_name>
ssh-keygen
ssh -T git@github.com
```

### Commands explained
`git --version` gives the version of git on the system. </br></br>
`git init` is used to make a directory as a git local repository. </br></br>
`git remote add origin "<ssh_link>"` or `git remote add origin "<html_link>"` used to connect our local repo to the remote repo on github. </br></br>
`git add <filename>` moves the file to staging area. </br></br>
`git add -A` moves all the untracked and modified files to staging area. </br></br>
`git status` gives the status of all files in the local repo. </br></br>
`git commit -m "<commit_message>"` used to commit a single file. </br></br>
`git commit -a -m "<commit_message>"` used to commit multiple files. </br></br>
`git pull origin master` used to pull all the files from remote repo to local repo. </br></br>
`git push origin master` used to push all the files from local repo to master branch. </br></br>
`git push origin <branch_name>` used to push files from remote repo to a subbranch named branch_name. </br></br>
`git log` used to see all the actions done. </br></br>
`git branch <branch_name>` used to create a branch. </br></br>
`git checkout <branch_name>` used to move to branch. </br></br>
`git checkout master` used to move back to master branch. </br></br>
`git checkout <first_eight_hexa> <filename>` used to revert back to previous version whose first eight hexadecimal digits are taken from log. </br></br>
`git merge <branch_name>` used to merge the work of branch_name to the master branch. Note that we should be in the destination branch before merging. </br></br>
`ssh-keygen` used to generate a key. </br></br>
`ssh -T git@github.com` used to authenticate the key. </br></br>




