
# Git

### Remove SSL verification
```
git config --global http.sslVerify false
```

### Add existing project 
```
git clone `webURL`
```

### Push code
```
git add *
git commit -m 'Pushing new code'
git push
```

### Move to remote branch
```
git fetch
git branch -a
git checkout -b `branch_name` origin/`branch_name`
```

### Stop asking for username and password
-Start by creating the ssh key
```
cd ~
ssh-keygen -t rsa
```
- Copy+paste the content of `~/.ssh/id_rsa.pub` into a Deploy Key in the Settings of the github repo
- Move to the project repo in the terminal
- Get the current project repo
```
git remote show origin
```
- Modify it so that it works
```
git remote set-url origin git+ssh://git@github.com/username/reponame.git
```
or as an example for the lab
```
git remote set-url origin git+ssh://git@githubifc.iad.ca.inet/UBI/ubi_weather.git
```

### Pull the branch that is stored on github, not locally
```
git pull origin `branch`
```

### Change branch
```
git checkout `branch`
```

### View branches
```
git branch
```

### Delete branch
```
git branch -D `branch`
```

### Retrive branch but don't merge it
```
git fetch -u origin `branch`
git push origin `branch`:`directory`
```

### Commit changes and close issue
```
git commit -m "Use functions : Close #3"
```

### Change name or move file
```
git mv `old file` `new file`
```

### View status of commit
```
git status
```

### Unstage
```
git reset HEAD
```

### Apply any commits of current branch ahead of specified one
```
git rebase origin/master
```

### Add changes to previous commit
```
git commit --amend
```

### Stage the removal of a file from a repo (and leave untracked file in working tree)
```
git rm --cached <filePath>
```

### Unstage any status change to a file
```
git reset -- <filePath>
```

