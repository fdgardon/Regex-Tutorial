# Regex-Tutorial
# Title (Regex-Tutorial)

A regular expression (also called regex or regexp) is a way to describe a pattern. It is used to locate or validate specific strings or patterns of text in a sentence, document, or any other character input. Regular expressions use both basic and special characters.

## Summary

The code I will be explaining is code to match a Hex Value. The snippet of the is code is `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`. This code is used to identifying colors.

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
In this particular case we are using two anchors or position meta characters in our regex: ^ and $.

The ^ meta characters represents the beginning of string or a line, and the $ represents the end of a string or a line. For example, ^abc will match any line or string that begins with abc, while xyz$ will match any line or string that ends with xyz.

Our regex uses these particular characters in combination to make sure that we are maching the full expresion from beginning to end.
### Quantifiers
This regex uses two types of quantifiers: ? and {n}.

The ? quantifier matches any preceding character 0 or 1 times. This makes the ? a sort of conditional inside regex. In our regex, since ? is preceded by #, our expression will match either a string that begins with # or not. Another example using ? would be:

regex: \w+ou?r would match both "favor" and "favour".

The other quantifier used in our regex is {n}, which is used twice ({6} and {3}). This meta character matches exactly the preceding character n-times. For example: {\d{4}} this regular expresion will match any string that has 4 consecutive digits like 1234 or 5555.
### Grouping Constructs
None
### Bracket Expressions
This regex expresion has one big group: ([a-f0-9]{6}|[a-f0-9]{3}). This grouping is used in combination with an OR operator, which is why I will explain it's purpose in that section.
### Character Classes
In our regex we have one character class that is repeated twice: [a-f0-9]. A character class matches any character enclosed in brackets. For example: [abc] will match "a" or "b" or "c". [-.] will match "-" or ".".

Inside our character class we have two ranges: a-f and 0-9. This means that it maches any character "a" through "f" (lowercase, it won't match uppercase), and "0" through "9". Other examples: [m-p] matches "m", "n", "o" or "p". [3-5] matches "3", "4" or "5".
### The OR Operator
As I mentioned in the grouping section, our regex has one big group, divided by an OR operator |. In the group ([a-f0-9]{6}|[a-f0-9]{3}) we have two expresions: [a-f0-9]{6} and [a-f0-9]{3}. This means that our regex will match any of those two expresions. Another use example for the OR operator is using it to validate email domains, for example (.com|.net|.org) wil match those ".com", ".net" or ".org", as part of an email address.
### Flags
None
### Character Escapes
The \ is known as the escape code, which restore the original literal meaning of the following character. Similarly, * , + , ? (occurrence indicators), ^ , $ (position anchors) have special meaning in regex. You need to use an escape code to match with these characters.
## Author
This is Farid Gardoon and I am student at UC Davis Coding Boot Camp that is going to end by 5 weeks, you can reach out to me by: https://github.com/fdgardon

## Depoly Link: https://gist.github.com/fdgardon/00cafbc178f896b3ec6dc8bef1e034bb
