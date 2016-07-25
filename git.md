
## Global configuration
* git config --global user.name "Will Dearman"
* git config --global user.email will@willdearman.com

## Adding a remote repo locally
* mkdir [name_here]
* cd [name_here]
* git init
* git remote add [name_here] https://github.com/willdearman/[name_here].git
* git pull [name_here] master

## Adding to the repo
* git add .
* git commit -m "Message here"
* git push'

-----
## Add existing local repo to github
* cd to local directory
* initialize local repository '''git init'''
* add files to stage for commit '''git add .'''
* first commit '''git commit -m "First commit"'''
* add and verify remote
'''
git remote add origin remote repository URL
git remote -v
'''
* Push local commit to repo '''git push origin master'''
