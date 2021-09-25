# Matching an email pattern in Regex

The term "Regex" stands for "Regular expressions" which are strings defining a pattern. They are used in different programming languages: JavaScript, PHP, Python, Perl and Java.
In JavaScript, RegEx are objects which are defined in Literals or Classes.

## Summary

In this tutorial would discuss: RegEx for Email.

>/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

Regex Components include Anchors, Quantifiers, Grouping constructs, character classes, character escapes, flags, OR operator. 

The email Regex includes following Components:

 ![Email Regex](/images/email-regex.jpg)

### Anchors ^ or $

*Preceed the string defining the character pattern
*For Email RegEx, we have ^ (Circumflex) anchor in the begining and $ at the end of email pattern.

### Grouping Constructs ()

*Used for complex Regex, where the pattern has to be matched in different sections.
*A typical valid email pattern is:
>somename@domain-name
>Ex. somename@email.com

*To follow the same pattern, the email RegEx has been grouped in 3 constructs:

1. ([a-z0-9_\.-]+)
2. ([\da-z\.-]+)
3. ([a-z\.]{2,6})

### Bracket Expressions []

*define range of characters to be matched
*[a-z0-9_\.-]: accepts characters a-z, numbers 0-9, special characters: "." and "-"
*[\da-z\.-]: \d - a digit 0-9, characters a-z, special characters: "." and "-"
*[a-z\.]: characters a-z and special character "."
*RegEx is case sensitive so email address in format **TOM@somemail.com** is **unacceptable**.
*Few accepted patterns are:
    *_abc@email.com
    *1bc@e1mail.net
    *abc@email.com
    *abc@2chan.co.gv

### Quantifiers {}

*Define the minimum and maximum number of times the defined pattern can be matched.
*For grouping construct 3, pattern is: ([a-z\.]{2,6}), which means that minimum 2 and maximum 6 characters from a to z can be entered followed by a period "."
*That mean, for email regex pattern, following formats are accepted: 
>/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
    *example@example.com
    *example@ca.ca
    *abc@2chan.co.gv

### Character Classes

*A character class is a special notation that matches any symbol from a certain set.
*They can be used to match digits(\d), words(\w) or spaces(\s).
*For email regex, the character class - git can be seen in construct -2:
> ([\da-z\.-]+)
*In this class, a single digit from 0-9 can be matched. 
*Examples:
    *example@99acres.com
    *example@w3c.com


### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
