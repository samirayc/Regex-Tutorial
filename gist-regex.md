# Matching an Email Using Regex

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

A grouping construct in regex is used to separate the regex into subexpressions to either help simplify a complex pattern or to extract a subset of information in a regex. In this regex, ```()``` parentheses are used to capture a group, breaking it down into three parts. The first set of the regex, ```([a-z0-9_\.-]+)``` is the username of the email address. The second set, ```([\da-z\.-]+)```, captures the email domain name, while the third set, ```([a-z\.]{2,6})``` captures the domain.

### Bracket Expressions

Bracket expressions in regex are a list of character and/or character classes that are enclosed in brackets ```[]```. These expressions are used in matching single characters or a range of characters in a list. In our email-matching regex there are three different bracket expressions that show the valid characters that can be substituted in the regex. The first is ```[a-z0-9_\.-]```, which defines valid characters as being ```a-z```, ```0-9```, and the symbols: ```_```,  ```.```, or ```-```. The second bracket expression, ```[\da-z\.-]```, as well as the third, ```[a-z\.]```, are used in the same exact way as the first (to define valid characters).

### Character Classes

Character classes are found within bracket expressions that distinguish kinds of characters, such as distinguishing between letters and digits. This regex uses the character class ```\d``` which denotes any digit character 0-9. The ```\``` indicates "character class".

### The OR Operator

An OR operator ```||``` is a boolean operator used to return the value as true if one or both of the values are true, and returns false otherwise. There is no use of the OR operator in the email-matching regex.

### Flags

Flags are optional parameters that you can add to regex to change its default way of searching. This email-matching regex has two flags that also function as the anchors: ```^``` and ```$```. These flags are an "input boundary assertion", with an "input boundary" being the start and end of the string. ```^``` asserts the beginning of the string while ```$``` asserts the end, similar to its use as an anchor. 

### Character Escapes

Character escapes are used to use a special character as a regular one, such as in situations when the desire is to match a character that cannot easily be represented in its literal form (ex: a line break). There is no use of a character escape in this email-matching regex.

## Author

Hi, I'm Samira Chetta and I'm the author of this tutorial! You can check out my GitHub profile [here](https://github.com/samirayc).
