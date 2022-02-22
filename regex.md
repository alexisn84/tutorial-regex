# Regex: Matching Values using Hex

Expressions are similar to patterns in that they used character combinations to match in strings. A typical expression using the the ^; this symbol ^ is a metacharacter and means "not". For example "a" equates to match lowercase "a", while "^a" has the opposite effect and means to not match lowercase "a".

## Summary

This tutorial is to help the user further understand the components of a regular expression using match `Hex Values`. A Hexidecimal code is a system that any specific color can be expressed to a computer(machine), thus bringing consistency in electronic displays regardless of external factors such as human languages and computer languages. A hexadecimal color code follows the pattern of a `#` followed by a six-digit code. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
`^#?([a-f0-9]{6}|[a-f0-9]{3})$`

Anchors match a position before, after, or between characters sothat they can be used to `“anchor”` the regex match at a certain position. The caret `^` matches the position before the first character in the string. Applying `^a` to <mark>abc</mark> matches `a`. Therfore, `^b` does not match <mark>abc</mark> at all, because the `b` cannot be matched right after the start of the string, matched by `^`. See below for the inside view of the regex engine. Similarly, `$` matches right after the last character in the string. `c$` matches `c` in <mark>abc</mark>, while `a$` does not match at all.

### Quantifiers
Quantifiers are used to communicate how many characters are expected. Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. By default, quantifiers are excessive, and will match as many characters as possible. If the `",+,?,{}"` characters are found within regular expressions, they are considered quantifiers. The `? `indicates the expression to match 0 or 1 time. There are basically 2 types of formats, so the `or` operator is used to distinguish which format the user is using.

Example:
In the Hex Value regular expression:
- /^#?([a-f0-9]{6
- [a-f0-9]{3})$/

There is `{6} (Hex Triplet Format)` and `{3} (Shorthand Hex Format)`, this indicates that the length of the component preceding these quantifiers should be 6 for `{6}` and 3 for `{3}`.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)