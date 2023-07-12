# Regular Expression (Regex) Tutorial - Matching an Email

In this tutorial, I will be walking you through the regular expression, or regex for short, pattern for validating/matching an email address.

## Summary

Specifically, I'll break down each of regex components and explain their role in the validation process of an email. 

Hopefully, by the end of this tutorial, you will have an understanding grasp of email validation with regular expressions, allowing you to do so in the futue on your own.

To start, here is the Regex Pattern for an Email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

Firstly, before delving into the regex components themselves, important to note is that a regex is considered a literal, so any regex patterns must be wrapped in slash characters (/), i.e there must be a slash on either end of them.

That of emails is no different, as evidenced below:

(NOTE: There are spaces added between the slashes and rest of the pattern for emphasis. These are not actually present in the pattern itself)

<b>/</b> ^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$ <b>/</b>

### Anchors

Both the $ (dollar sign) and ^ (caret) characters are considered anchors in the context of regex.

The ^ signifies a string that starts with the characters that follow it.

The $ signifies a string that ends with the characters that precede it. 

Both of these anchors can either be followed/preceded by an exact string or a range of possible matches.

In the example of our email regex, the matching strings we will be looking for matches the patterns:

[a-z0-9_\.-], [\da-z\.-], and [a-z\.]

The various other components are quantifiers which don't fall under the anchor's umbrella and will be addressed below.

### Bracket Expressions

Bracket Expressions refer to patterns inside a set of square brackets ([]), with anything inside of them being a set of characrers we want to match or include. For this reason, Bracket Expressions are also known as the positive character group.

[a-z0-9_\.-], [\da-z\.-], and [a-z\.] are all bracket expressions and can be broken down as followed:

[a-z0-9_\.-]

* [a-z]: The corresponding string can contain any lowercase letter between a–z, but ONLY lowercase letters

* [0-9]: The corresponding string can contain any number between 0–9

* [_\.-] The corresponding string can contain the special characters: underscore (_), backslash (\), period (.), and hyphen (-)

* Examples fitting this criteria: "Kane13", "Ka_n3\", "1337."

[\da-z\.-]

* [\d]: A character class which will be addressed below; for all intents and purposes, it's equivalent to [0-9] which was covered above.

* [a-z]: See above

* [\.-]: The corresponding string can contain the special characters: backslash (\), period (.), and hyphen (-)

* Examples fitting this criteria: "gmail", "comcast", "hotmail."

[a-z\.]

* [a-z] See above

* [\.] The corresponding string can contain the special characters: backslash (\) and period (.)

* Examples fitting this criteria: "com", "net", "gov"

### Quantifiers

Qunatifiers are used the limits of the string that either the entire regex or an individual section of the regex's string matches.

Specifically, the Quantifers being used in the email regex:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Are as followed:

The Plus Sign (+) and Curly Brackets ({}) which are explained as followed:

* ([a-z0-9_\.-]+): Matches the Pattern in the Bracketed Expression one or more times

* ([\da-z\.-]+): See Above

* ([a-z\.]{2,6}): Matches the pattern in the Bracket Expression from a minimum of 2 times to a maximum of 6 times.


### Grouping Constructs

Grouping Constructs are a means of truncating off different parts of a string via parentheses () into subexpressions so that they are subject to different restrictions.

([a-z0-9_\.-]+), ([\da-z\.-]+), and ([a-z\.]{2,6}) are all subexpressions.

In the primary email pattern:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

An @ symbol seperates ([a-z0-9_\.-]+) from ([\da-z\.-]+) which is seperated from ([a-z\.]{2,6}) via a period (.).

The backlash attached to said period is a character escape and will be defined below.

Examples of the email pattern with Grouping Constructs in mind:

"k1ayng24@gmail.com", "kan327@comcast.net", "1337@hotmail.gov"

### Character Classes

Character Classes within a regex define sets of characters, with any one of said characters being able to occur in an input string to fulfill a match.

Within the context of

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
