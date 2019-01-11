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

### Stop asking for username and password
-Start by creating the ssh key
```
cd ~
ssh-keygen -t rsa
```
- Add `~/.ssh/id_rsa.pub` as a key in the account settings on the github website
- Get the current project repo
```
git remote show origin
```
- Modify it so that it works
```
git remote set-url origin git+ssh://git@github.com/username/reponame.git
```
