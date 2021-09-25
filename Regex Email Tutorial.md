# Matching an email pattern in Regex

The term "Regex" stands for "Regular expressions" is, in theoritical computer science a sequence of characters that define a search pattern. Given an input string, it is validated through a pattern expression.

## Summary

This tutorial talks about use of regular expressions to match internet email addresses using the following regex:

>/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Many frameworks and applications use above pattern to validate email addresses.

## Table of Contents

- [Anchors](#anchors)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Character Classes and Escapes](#character-classes-and-escapes)

## Regex Components

Regex Components include Anchors, Quantifiers, Grouping constructs, character classes, character escapes, flags, OR operator. 

The email Regex includes following Components:

 ![Email Regex](/images/email-regex.jpg)

### Anchors

Preceeds or succeeds the string defining the character pattern
In Email regex, the `^` (Circumflex) anchor is placed at the beginning of the string and `$` indicates the end of string.

### Grouping Constructs

Grouping constructs are used for complex regex, wherein the pattern has to be matched in different sections.
A typical valid email address is:

>somename@domain-name
>Ex. somename@email.com

To follow the same pattern, the email regex has been grouped in 3 constructs:

1. ([a-z0-9_\.-]+) - This will match the user email name.
2. ([\da-z\.-]+) - This will validate email service/ domain name.
3. ([a-z\.]{2,6}) - This construct will validate the remaining domain name such as `.com`, `.net`, `.gov` or a 2 character like `.co`, `.in`.

### Bracket Expressions

Bracket expressions help in validating range of characters.Below are some bracket expressions used in email regex.

- [a-z0-9_\.-]: accepts characters a to z, numbers 0 to 9, special characters: ".", "_" and "-"
- [\da-z\.-]: \d - a digit 0 to 9, characters a to z, special characters: "." and "-"
- [a-z\.]: characters a to z and special character "."

One important thing to note is that regex is case sensitive. So email address in format TOM@somemail.com is unacceptable.
Few accepted patterns are:
    - a_bc@email.com
    - 1bc@email.net
    - abc@email.com
    - abc@chan.co.gv

### Quantifiers

Quantifiers in regular expressions define the minimum and maximum number of times the defined pattern can be matched.
For grouping construct 3, pattern is: ([a-z\.]{2,6}), which means that minimum 2 and maximum 6 characters from a to z can be entered followed by a period "."
This means, for email regex pattern, following formats are accepted:
    - example@example.com
    - example@test.ca
    - abc@chan.co

### Character Classes and Escapes

A character class is a special notation that matches any symbol from a certain set.
They can be used to match digits(\d), words(\w) or spaces(\s). A backslash(\) character in a regex preceeds literal character.
Certain letters can be escaped by representing common character classes, such as `\w` for a word character or `\s` for a space.
For email regex, the character class `\d` is seen in second construct

> ([\da-z\.-]+)

In this class, a single digit from 0-9 can be matched.
Examples:
    - example@99acres.com
    - example@w3c.com

## Author

This email regex tutorial is created by Kalyani Joshi.
GitHub: [kay-code-1](https://github.com/Kay-code-1)
