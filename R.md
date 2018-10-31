# Grep multiple patterns
```
pattern = c('a1, 'a3', 'a5')
result = grep( paste(pattern, collapse='|'), data)
```

# Add leading zeroes
```
require(stringr)
str_pad(imonth, 2, pad="0")
```

