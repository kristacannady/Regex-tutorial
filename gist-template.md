# Regex-Tutorial: 

What is a Regex? A Regex, also known as a regular expression, is a sequence of characters that forms a search pattern. These strings of text can be used for search functions to find and manage certain text. They can also be used to validate input. 

Although they look daunting, this tutorial will break down a certain Regex to show their value within the programing world. 

## Summary: Hex 

The following expression is used to match HEX values:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Within this tutorial, the anchors, quantifiers, OR Operator, character classes, grouping and capturing, bracket expressions, and greedy/lazy match are broken down to better understand the usage of this Regex. 

This regex is able to match a hex value such as: 555, #a54, abcdef, and more. 

The expression means the regex can match a hex value:
- With or without a # symbol
- 3 or 6 characters long 
- Any number 0-9
- Any lowercase letter a-f 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Author](#Author)

## Regex Components

### Anchors

Anchors help with the search process by asserting information about the string. 

`^` anchor indicates what the string must start with. 
Example: `^This` means the string must begin with `This`

`$` indicates what the string must end with. 
Example: `End$` means the string must begin with `End`

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The string needs to match with the 3 or 6 character pattern identified before the `$` anchor. 

### Quantifiers

Quantifiers define how many times a character must be present in the match that is being searched for. 

`{n}` means that the character matches exactly `n` times. 
'?' means the preceding character is optional. 

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
`{6}` means the string will contain 6 characters. 
`?` means that the character `#` is optional.
`{3}` means that the string will contain 3 characters. 

### OR Operator

The OR operator, `|` or `[]` is a boolean that allows different paramaters to be allowed and/or searched for. 

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The OR operator means that our string will either have 3 or 6 characters. 

### Character Classes

Character classes define the characters that can be used. This is marked by the `-` character. 
IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
 `[a-f0-9]` means that the characters being searched for are lowercase a-f and 0-9. 

### Grouping and Capturing

By using the `()` character, grouping allows you to apply quantifiers to an entire group. 

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The grouping allows for the quantifier of `{6}` or {3} to be applied to all of the characters. 

### Bracket Expressions

Bracket expression matches a certain pattern of characters that is defined within brackets `[]`. 

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The brackets here indicate matching a string that has lowercase a-f or 0-9. 

### Greedy and Lazy Match

Greedy Match is finding the longest possible string. Lazy match means finding the shortest possible string. 

Normal quantifiers `{}` (quantifiers define how many times a character must be present in the match that is being searched for) are greedy. Although, if `?` was appended, the quantifier would become lazy. 

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` 
The quantifier is greedy, meaning it wants to match as many digits as it can. 

## Author

My name is Krista Cannady. I am learning programming and web technologies to advance my career in healthcare by branching into technology. Find more of my projects at https://github.com/kristacannady. 