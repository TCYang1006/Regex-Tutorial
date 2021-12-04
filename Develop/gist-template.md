# Beginners Introduction to Regex
This is a beginner's guide to Regex "Regular Expressions".  The tutourial will teach you to create powerful time saving regex.  These tutorials are fundamental regexes which will allow you to build more complex regexes down the road.  Take the time to understand the fundamental regexes.

## Summary
Regex is a sequence of characters that defines a specific search pattern.  When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string.  Regex are often used to validate inputs.  

## Table of Contents
-[Anchors](#Anchors)  
-[Quantifiers](#quantifiers)  
-OR Operator
-Character Classes
-Flags
-Grouping and Capturing
-Bracket Expressions
-Greedy and Lazy Match
-Boundaries
-Back-references
-Look-ahead and Look-behind
-Regex Components
-Anchors
-Quantifiers
-OR Operator
-Character Classes
-Flags
-Grouping and Capturing
-Bracket Expressions
-Greedy and Lazy Match
-Boundaries
-Back-references
-Look-ahead and Look-behind

## Description of regex components

### Anchors  
Anchors are characters used to match strings that starts, ends or find exact match.  Regex uses `^` and `$` as anchors.
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

## Author
A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
