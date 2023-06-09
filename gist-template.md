# Regular Expression Components

Regular expressions, also known as regex, are a sequence of characters that define a search pattern. They are commonly used in text processing and pattern matching. In this README, we will discuss the various components that make up regular expressions.

## Summary

Here we have a code snippet of a regular expression that is used to validate whether a string matches the format of an email address.
    /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

    ^ - Matches the start of the input string
    ([a-z0-9_.-]+) - Matches one or more characters that are lowercase letters, digits, underscore, hyphen or period, and captures them in a group
    @ - Matches the '@' symbol
    ([\da-z.-]+) - Matches one or more characters that are digits, lowercase letters, hyphen, or period, and captures them in a group
    . - Matches a literal period (.)
    ([a-z.]{2,6}) - Matches two to six characters that are lowercase letters or a literal period, and captures them in a group
    $ - Matches the end of the input string    


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
Regular expressions, also known as regex, are a sequence of characters that define a search pattern. They are commonly used in text processing and pattern matching. In this README, we will discuss the various components that make up regular expressions.

### Anchors
Anchors are used to specify the position of a match in a string. They are denoted by the caret (^) and dollar sign ($). Here are some examples of anchors:

    ^ (caret): matches the beginning of a string
    $ (dollar sign): matches the end of a string

### Quantifiers
Quantifiers are used to specify how many times a character or group should be matched. They are denoted by curly braces { }. Here are some examples of quantifiers:

    {n}: matches the preceding character n times
    {n,}: matches the preceding character at least n times
    {n,m}: matches the preceding character between n and m times

### OR Operator
OR operator is used to combine two or more conditions or expressions, and it returns true if at least one of the conditions is true.
    Here's how the OR operator works:

    If both expressions are true, the OR operator returns true.
    If only one expression is true, the OR operator returns true.
    If both expressions are false, the OR operator returns false.


### Character Classes
Character class is a set of characters that are enclosed in square brackets and used to match any one character from that set.
Here are some common character classes and what they match:

    [a-z]: matches any lowercase letter from a to z.
    [A-Z]: matches any uppercase letter from A to Z.
    [0-9]: matches any digit from 0 to 9.
    [a-zA-Z]: matches any letter, whether uppercase or lowercase.
    [\d]: matches any digit character.
    [\D]: matches any non-digit character.
    [\s]: matches any whitespace character, including spaces, tabs, and line breaks.
    [\S]: matches any non-whitespace character.
    [\w]: matches any word character, including letters, digits, and underscores.
    [\W]: matches any non-word character.


### Flags
Flags are optional parameters that can be added to the end of the expression to modify how the pattern is matched.
    g (global): This flag causes the regular expression engine to find all matches in the input string, instead of stopping after the first match.
    i (ignore case): This flag causes the regular expression to ignore the difference between uppercase and lowercase letters when matching.
    m (multiline): This flag causes the "^" and "$" anchors to match the start and end of each line in a multi-line input string, instead of just the start and end of the entire input string.
    s (dotall): This flag causes the "." metacharacter to match any character, including line breaks.
    u (unicode): This flag enables support for Unicode characters in the regular expression.
    y (sticky): This flag causes the regular expression to match only at the position in the input string indicated by the lastIndex property of the regular expression object.

### Grouping and Capturing
Grouping is a feature in regular expressions that allows you to group multiple characters or patterns together and treat them as a single unit. Grouping is done by enclosing the characters or patterns in parentheses ( and ). Capturing is a feature in regular expressions that allows you to extract specific parts of a matched string. Capturing is done by enclosing the part of the regular expression you want to capture in parentheses ( and ).

### Bracket Expressions
Bracket expressions, also known as character classes, are a feature of regular expressions that allow you to match any one character from a set of characters. A bracket expression is enclosed in square brackets [ ] and contains a list of characters or character ranges that you want to match.

### Greedy and Lazy Match
A "greedy" quantifier will match as much as possible, while still allowing the overall pattern to match. For example, the pattern ".*" is greedy, and will match any number of characters, as long as the overall pattern still matches. This means it will match as much as possible, which can be useful in some cases.

A "lazy" quantifier, on the other hand, will match as little as possible, while still allowing the overall pattern to match. For example, the pattern ".*?" is lazy, and will match as few characters as possible, again as long as the overall pattern still matches. This can be useful in cases where you want to match a specific substring that appears multiple times in the text, but you only want to capture the first occurrence.

### Boundaries

In regular expressions, boundaries are used to specify the edges of a word or line of text. There are two types of boundaries:

Word boundaries: These boundaries are used to match the beginning or end of a word. The symbol for a word boundary is "\b". For example, the regex pattern "\bcat\b" will match the word "cat" but not "cats" or "scat".

Line boundaries: These boundaries are used to match the beginning or end of a line of text. The symbol for a line boundary is "^" for the beginning of a line and "$" for the end of a line. For example, the regex pattern "^Hello" will match any line of text that begins with "Hello", while the pattern "world$" will match any line of text that ends with "world".

### Back-references
Back-references in regular expressions refer to previously matched groups in the pattern. When you use parentheses in a regular expression, the text that matches the expression inside the parentheses is captured as a group. You can then reference that group later in the pattern using a back-reference. The syntax for a back-reference is a backslash followed by the number of the group.

### Look-ahead and Look-behind
Look-ahead and look-behind are advanced concepts in regular expressions that allow you to search for patterns that are either preceded or followed by another pattern, without actually matching the pattern in the search result. These concepts are denoted by the special symbols (?=) for look-ahead and (?<=) for look-behind.

Look-ahead assertion (?=pattern): This matches a group of characters that are followed by another specific pattern. It is useful when you want to match a pattern only if it is immediately followed by another specific pattern. For example, the regular expression "a(?=b)" matches the letter "a" only if it is immediately followed by the letter "b".

Look-behind assertion (?<=pattern): This matches a group of characters that are preceded by another specific pattern. It is useful when you want to match a pattern only if it is immediately preceded by another specific pattern. For example, the regular expression "(?<=a)b" matches the letter "b" only if it is immediately preceded by the letter "a".

### Author
- [@tjb47-dev](https://github.com/tjb47-dev)