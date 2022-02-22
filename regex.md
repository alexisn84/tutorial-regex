# Regex: Matching Values using Hex

Expressions are similar to patterns in that they used character combinations to match in strings. A typical expression using the the `^`; this symbol `^` is a metacharacter and means `not`. For example `a` equates to match lowercase `a`, while `^a` has the opposite effect and means to not match lowercase `a`.

## Summary

This tutorial is to help the user further understand the components of a regular expression using match `Hex Values`. For example one of the uses of `Hex Values` is the `Hexidecimal code`, a system that any specific color can be expressed to a computer(machine), thus bringing consistency in electronic displays regardless of external factors such as human languages and computer languages. A hexadecimal color code follows the pattern of a `#` followed by a six-digit code. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)

## Regex Components

### Anchors
`^#?([a-f0-9]{6}|[a-f0-9]{3})$`

Anchors match a position before, after, or between characters sothat they can be used to `“anchor”` the regex match at a certain position. The caret `^` matches the position before the first character in the string. Applying `^a` to <mark>abc</mark> matches `a`. Therfore, `^b` does not match <mark>abc</mark> at all, because the `b` cannot be matched right after the start of the string, matched by `^`. See below for the inside view of the regex engine. Similarly, `$` matches right after the last character in the string. `c$` matches `c` in <mark>abc</mark>, while `a$` does not match at all.

### Quantifiers
Quantifiers are used to communicate how many characters are expected. Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. By default, quantifiers are excessive, and will match as many characters as possible. If the `",+,?,{}"` characters are found within regular expressions, they are considered quantifiers. The `? `indicates the expression to match 0 or 1 time. There are basically 2 types of formats, so the `or` operator is used to distinguish which format the user is using.

`Example:`
In the Hex Value regular expression:
- /^#?([a-f0-9]`{6}`
- [a-f0-9]`{3})`$/

There is `{6} (Hex Triplet Format)` and `{3} (Shorthand Hex Format)`, this indicates that the length of the component preceding these quantifiers should be 6 for `{6}` and 3 for `{3}`.

### OR Operator
The `or` operator within a regular expression is defined using the `| `element (found on the keyboard above the `Enter` key). The `or` operator indicates that it could either of the components that the user is separating with the `|`. For the hex value regular expression of have ([a-f0-9]{6}``|``[a-f0-9]{3}). Note the `or` operator separating these 2 components. This means that the hex value could either be 6 characters `[a-f0-9]{6}` or 3 characters` [a-f0-9]{3}`.

### Character Classes
Character classes are components within the regular expression that tells the code/user what type of characters to expect. The example shows character classes are confined within brackets []. For the example there are 2 character classes: `[a-f0-9]` and `[a-f0-9]` which searches for the same values. The breakdown of what it is searching for is as follows: `a-f` searches for letters `a-f` and `0-9` searches for digits `0-9`.

### Bracket Expressions
Matches any character in the square brackets. 

### Greedy and Lazy Match
A greedy match tries to match an element as many times as possible. Whereas, a lazy match tries to match an element as few times as possible. In the above example there is `?` which signifies lazy quantifier. This is referred to a lazy quantifier because it causes the regular expression engine to match as few occurances as possible. 

## Author

You can find more of my works at [GitHub](https://github.com/alexisn84), thank you for reading! -Alexis