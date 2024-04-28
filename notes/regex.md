## Regular Expressions

- Regex is a pattern-matching language.
- Used for different types of text processing problems.

- ```s/``` in sed, vim, perl means substitution


### Regex in JS

- str.split(re)
- str.match(re)
- str.replace(re)
- re.test(str)
- re.exec(str)


### Escaping metacharacters

In js and perl generally we don't need to escape metacharacters. To have similar resut in sed and grep, use:

- ```sed - r```
- ```grep - E```

Otherwise it is necessary to escape characters, except '*'.


### Flags

- ```i ``` - case insensitive
- ```g ``` - match all occurences (global)
- ```m ``` - treat string as multiple lines
- ```s ``` - treat string as a single line


### Metacharacters

- ```[]``` - character class
- ```^```  - anchor at the beginning
- ```$```  - anchor at the end

- ```(a|b)``` - match a or b

- ```()```   - capture group
- ```(?:)``` - non capture group

- ```\d```   - digi ```[0-9]```
- ```\w```   - word ```[A-Za-z0-9_]```
- ```\s```   - whitespace ```[ \t\r\n\f]```


### Quantifiers

- ```.```  - matches any character
- ```?```  - zero or one time
- ```*```  - zero or more times
- ```+```  - one or more times
- 
    - ```{2, 4}``` number of characters should be between 2 and 4 characters.
    - ```{2,}``` number of characters should be at least 2 characters



### Character class sequences

- ```\w``` - word character: ```[A-Za-z0-9_]```
- ```\W``` - non-word character: ```[^A-Za-z0-9_]```
- ```\s``` - whitespace: ```[ \t\r\n\f]```
- ```\S``` - non-whitespace: ```[^ \t\r\n\f]```
- ```\d``` - digit: ```[0-9]```
- ```\D``` - non-digit: ```[^0-9]```


### Anchors

- ```^``` - anchor at the beginning
- ```$``` - anchor to the end


### Groups

- ```()```   - capture group
- ```(?:)``` - non capture group
