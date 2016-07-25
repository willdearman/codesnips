## Approach
Ideally, you should never make any commits directly to the master branch of your fork or the local repository. This branch must only be used for keeping the updated code from upstream. All changes must be made to new feature or bug branches, and pushed to the branches with the same name on the fork.

Thus you need to update the fork with the latest commits from the central repository:

1) Pull from upstream’s master branch to local repository’s master
2) Push from local repository’s master to fork’s master
3) These steps assume that you have forked the repository and cloned the fork on your local machine.

When you have your project at a point that you want to share, you have to push it upstream. The command for this is simple: git push [remote-name] [branch-name].


## Initial Steps
````
mkdir talentbot
cd talentbit
git init
git clone git@github.com:howdyai/botkit.git

git remote add upstream git@github.com:howdyai/botkit.git

git remote add origin git@bitbucket.org:willdearman/talentbot.git
git push origin master
````

## Maintenance Steps
````
git pull upstream master
git merge upstream/master
git push origin master
````
---
