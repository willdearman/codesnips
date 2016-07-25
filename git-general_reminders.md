
## Global configuration
* ``` git config --global user.name "Will Dearman" ```
* ``` git config --global user.email will@host.local ```

## Adding a remote repo locally
```
mkdir [name_here]
cd [name_here]
git init
git remote add [name_here] https://github.com/willdearman/[name_here].git
git pull [name_here] master
```

## Adding to the repo
````
git add .
git commit -m "Message here"
git push
````

## Add existing local repo to github
1) cd to local directory

2) initialize local repository ```git init```

3) add files to stage for commit ```git add .```

4) first commit ```git commit -m "First commit"```

5) add and verify remote
```
git remote add origin remote repository URL
git remote -v
```

6) Push local commit to repo ```git push origin master```
