# File archiving

### Put files in a .tar.gz
```
tar -czvf `archive`.tar.gz *.csv
```
### View pretty JSON file
```
cat `filename`.json | python -m json.tool
```

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

### Move to remove branch
```
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
