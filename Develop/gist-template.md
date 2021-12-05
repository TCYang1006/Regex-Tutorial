# Beginners Introduction to Regex
This is a beginner's guide to Regex "Regular Expressions".  The tutourial will teach you to create powerful time saving regex.  These tutorials are fundamental regexes which will allow you to build more complex regexes down the road.  

## Summary
Regex is a sequence of characters that defines a specific search pattern.  When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string.  Regex are often used to validate inputs.  The  fundamental regexes in the Table of Contents are used to match a URL.  Review the fundamental regexes indiviually to get an better understanding of how it is used to validate a URL.

## Table of Contents  

[Character Classes](#CharacterClasses)  
[Anchors](#Anchors)   
[Quantifiers](#Quatifiers)  
[OR Operator](#OROperator)  
Flags  
Grouping and Capturing  
Bracket Expressions  
Greedy and Lazy Match  
Boundaries  
Back-references  
Look-ahead and Look-behind  
Anchors    
OR Operator  
Character Classes  
Flags  
Grouping and Capturing  
Bracket Expressions  
Greedy and Lazy Match  
Boundaries  
Back-references  
Look-ahead and Look-behind  
  
## Understanding the Fundamentals of Regexs  
  
### <ins>Character Classes<ins>  
Character classes are symbol from a certain character set.  
`.` is the character class for any single character  
`\d` is the symbol for digits or a character 0-9  
`\w` is a word character that matches the ASCII characters A-Z, a-z or 0-9  
`\s` is the symbol for space, tab and newline  
  
Examples of Character Classes:
```
Coding 101 is an awsome class!

Use the above sentence to help understand character classes.  
A pattern /C./g  (The dot is any single character after the capital "C") will return Co  

A pattern /\d/g (The "\d" is look for the 1 digit) will return 1, 0, 1 
A pattern /\d\d/g (The 2 "\d" is looking for 2 digits) will return 10
A pattern /\d\d\d/g (The 3 "\d" is looking for 3 digits) will return 101

A pattern /\w/g (The "\w" is looking for any 1 letter or digit in a word) will return C, o, d, i, n, g, 1, 0, 1, i, s, a, n, a, w, s, o, m, e, c, l, a, s, s  (notice the exclamation mark is not included)
A pattern /\w\w\w\w/g (The 4 "\w" is looking for any word with at least 4 letters) will return Codi, awes and clas 
A pattern /\w\w\w\w\w\w\w/g (The 7 "\w" is looking for any word with atleast 7 letters) will return awesome

A pattern /\s/g (The "\s" is looking for a space, tab or newline) will return 5 spaces
```


### <ins>Anchors<ins>  
Anchors are positioning characters used to match strings that starts, ends or find exact match.  Regex uses `^` and `$` as anchors.
The anchor `^` is use to match any string that starts after the character `^`.
The anchor `$` is use to match any string that ends after the character `$`.
Using both anchors `^` and `$`, will find any string with the exact match.
Without any anchors, will find any string that has the same values.

Examples of anchors:
```
^Cup :  matches any string that starts with Cup
Key$ :  matches any string that ends with Key
^Escape Club$ :  This is an exact string match (starts and ends with Escape Club)
morning :  matches any string that has the text morning in it
```
  

### <ins>Quantifiers<ins>
Quantifiers are used to determine how many character(s), group or character class needs to follow in order for a match.  Regex uses the following as quantifiers:  
`+` means match 1 or more  
`*` means match zero or more
`?` means match zero or 1
`{a, b}`: match from a to b times
`{n}`: match n times 
  
Examples of quantifiers:  
```   
Met is the past tense for Meet  

Use the above sentance for a better understanding of quantifiers.  
The quantifier + means 1 or more.  It is the same as {1,}.
A pattern /M+\g (This is saying search for 1 or more with the letter "M") will return M, M  

The quantifier * means zero or more.  It is the same as {0,}.
A pattern /M\w*/g (This is saying search for zero or more words (\w) starting with the letter "M") will return Met, Meet

The quantifier ? means zero or 1.  It is the same as {0, 1}.
A pattern /Me?et/g (This is saying search for zero or 1 that starts with "M" or "Me" with  "et" at the end; therefore, the e after the M is optional) will return Met, Meet  

The quantifier {1} means how many character or character class that needs to match.  
A pattern /Me{1}/g (This is saying search for a "M" and 1 "e") will return Me, Me

The quantifier {1,2} means the range matches a character or character class from 1 to 2 times.  
A pattern /Me{1,2}/g (This is saying search for "M" and 1 "e" or 2 "e") will return Me, Mee  
```

## Putting the Fundamental of regex to use
From the fundamental of regexes let's put this all together to understand how regexes uses the expression to match a URL.  

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`    

Let's start from the beginning and ending of the expression.  
`/` and `/`  
This define the regular expression boundary

The next character is ^.  This the anchor that defines the start of the expression.

Next, let's look inside of the parenthesis `(https?:\/\/)`.  The search will start with "h" "t" "t" "p" with an option for "s". Either https or http will be search.  After either http or https, there will be a ":".  After the ":" the 2 "\/" are literally "//".  Inside the parenthesis there are two options to search for:

- http://
- https://

The 

## Author
A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
