# Matching an Email using Regex

The regex we will be looking at in this Gist is used for validating email inputs in a given application. We will dissect this regex: ```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/``` into its basic components.

## Summary

Before we get into too much detail about a regex's components, firstly: What is a regex? A "regex", also known as a "regular expression" is a sequence of characters that is used to recognize and match patterns in text. Regex can be used in a lot of ways, some examples including: "find-and-replace" searches; finding data such as emails, phone numbers, usernames, etc. - anything that requires data-matching or searching data can be done easily with regex. In the case of the Regex we will be looking at today, it will be used to match and verify email addresses.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors in regex are either used to mark the beginning/end of a string or the beginning/end of a line. This is dependent on whether or not multiline is enabled. In our email regex, multiline is not enabled which means the anchor markers will indicate the start and end of a string as opposed to a line. This regex uses the anchors ```^``` which denotes the start of the string and ```$``` which denotes the end of the string.

### Quantifiers

In regex, quantifiers are used to tell how many times a part of the regular expression should be repeated. In our email-matching regex, there are two examples of different quantifiers that are used, the first of which being ```+```. This quantifier means "one or more", and in this particular case is used twice. The first ```+``` means one or more characters that satisfy the requirements of ```[a-z0-9_\.-]```, while the following ```+``` similarly denotes one or more characters in the group ```[\da-z\.-]```. The other quantifier used is ```{x, y}```, which in our email-matching regex, is presented as ```{2, 6}```. The ```x``` value represents the minimum value while the ```y``` value represents the maximum value, meaning that ```{2, 6}``` indicates two to six characters in the group ```[a-z\.]```. 


### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
