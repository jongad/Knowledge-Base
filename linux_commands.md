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
