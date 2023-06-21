# Email Regex - Gist

In this gist we will walkthrough what a regex (regular expression) is, and how to use them with a breakdown of each component pertaining to email. Regex are used to match certain character combinations inside a string. Coders use regex to pull information from given code bases and for validation during a login process. This tutorial will use a code snippet that would be used to find emails.

## Summary

The subsequent code will be utilized throughout the tutorial to provide explicit examples of how regex components can be employed. This code serves the purpose of email matching. One application of this code involves validating whether an email adheres to the correct format.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Author](#author)
- [Resources](#resources)

## Regex Components

### Anchors

Anchors are what start and end the regex. They are special characters or constructs that allow you to match patterns based on their position within the text rather than the actual content. <br>
As it pertains to the following code snippet:<br>
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br><br>
`/^` and `$/` are the anchors. Here the code is stating that we are looking for an email address that starts with: <br><br>
`([a-z0-9_\.-]+)` <br><br>
and ends with anything following the next piece of the code: <br>
`.([a-z\.]{2,6})` <br><br>
The email is not a match unless it adheres to the specific parameters stated above.

### Quantifiers

To establish a match, a quantifier is employed to ascertain the required number of occurrences for a particular character or group of characters. They allow you to define how many times a specific element should appear to consider a match.<br>
In reference to our code snippet:<br>
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`<br><br>
The Quantifiers:
`([a-z0-9_\.-]+)`<br>

In order to have a match, any string containing characters from `a-z`, `0-9`, `_`, `.`, or `-` can be matched. The `+` quantifier indicates that there must be at least one occurrence of these characters.

### Grouping Constructs

The code contains parentheses `()` to define three groups within the regular expression.<br>
The three groups are as follows: <br>

- Group 1: `([a-z0-9_\.-]+)`
  - Matches any combination of lowercase letters (`a-z`), digits (`0-9`), underscore (`_`), dot (`.`), or dash (`-`).
- Group 2: `([\da-z\.-]+)`
  - Matches any combination of digits (`\d`), lowercase letters (`a-z`), dot (`.`), or dash (`-`).
- Group 3: `([a-z\.]{2,6})`
  - Matches lowercase letters (`a-z`) or dot (`.`) with a length of 2 to 6 (`2,6`) characters.

### Bracket Expressions

In regular expressions, bracket expressions, also known as character classes, are used to define a set or range of characters that can be matched at a specific position within a string. <br> They are enclosed within square brackets `[ ]`.
Within a bracket expression, you can include individual characters or specify ranges using a hyphen `-` to represent a continuous sequence of characters.<br> For example, `[a-z]` represents all lowercase letters from 'a' to 'z'.

### Character Classes

Character classes are predefined sets of characters that match any single character within that set.<br>
They allow you to specify common groups or categories of characters without explicitlly listing each character individually.<br>
Character classes simplify pattern matching by providing shorthand representations for frequently used character sets. <br>
Character classes are denoted by special symbols or abbreviations inside square brackets `[]`. <br>
The code utilizes character classes `\d`, `\w`, and `.` to match specific sets of characters.

- `\d`: Matches any digit character (0-9).
- `\w`: Matches any word character (alphanumeric: a-z, A-Z, 0-9, and underscore).
- `.` (dot): Matches any character except a newline character.

### The OR Operator

In context of our code snippet we are using: <br>
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br>
There are no OR Operators. <br>
However, as it pertains to regex, an OR Operator is represented by a pipe symbol `|`. <br>
This allows you to match either one patter or another.

### Flags

In context of our code snippet we are using: <br>
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br>
There are no Flags. <br>
Flags are additional options that modify the behavior of the pattern matching. <br>
They are typically appended at the end of the regex and affect how the pattern is interpreted and applied.

### Character Escapes

In context of our code snippet we are using: <br>
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br>
There are two Character Escapes. <br>
Character Escapes use the backslash `\` followed by a specific character or define a special behavior. <br>
In regards to our code snippet:
The `\.` matches a literal dot (`.`) character, <br>
The `\d` matches any digit character from [`0-9`].<br>
Character Escapes are useful when you want to match characters that have a special meaning in regex, such as metacharacters or control characters, as literal characters.

## Author

This tutorial was created by Trace Martin. I was a teacher of 7 years now looking to change careers and move into the world of Tech. I am hopeful that this tutorial can shed some light on regular expressions and help guide others during their journey! <br>
[Github](https://github.com/trace-martin)

## Resources

[Regular Expression Tutorial](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial) <br>
[Introduction to Regular Expressions](https://www.youtube.com/watch?v=7DG3kCDx53c)
