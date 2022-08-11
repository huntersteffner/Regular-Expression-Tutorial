# Regular Expression Email Validator

Hello, and thank you for viewing this brief tutorial on using Regular Expressions, or Regex for short.

## Summary

Regular Expressions are patterns can be used to match strings with specific character combinations. While the Regular Expressions may look like random characters without any meaning at first, upon closer examination it is evident that each character has a special meaning. There is some variation between how Regular Expressions work with different programming languages, so for simplicity's sake, we will focus on JavaScript for this tutorial.

We will demonstrate how Regular Expressions work by showing how an email validator works. Below is the expression:

<code> /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ </code>

While this may look incoherent, remember that each character does have a purpose. The following components will explain how this works.

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

All regular expressions must start and end with <code>/</code>

### Anchors
The anchors specify the beginning and and end of the expression.

The <code>^ </code> anchor indicates the beginning of the expression.

The <code>$ </code> anchor indicates the end of the expression.

In the expression you can see how both anchors are used to indicate the start and beginning of what is being searched for.

### Quantifiers
Quantifiers show how many instances of a character, group, or character class must be present in a string. It is shown within <code>{}</code> and two numbers separated by a <code>,</code> show the minimum and maximum number of instances that must be present to pass the validation.

The <code>{2,6}</code> in the email Regular Expression shows that the closing domain tag must have at least two characters, but no more than six characters.

### Grouping Constructs
Grouping constructs break the expression down into subexpressions and capture the substrings of an input string.

These makes different sections within the expression that each have its own rules.

In JavaScript these are signified with <code>()</code>.

There are three of these subsections in the email validator above.

### Bracket Expressions
Bracket Expressions show the range of characters that are allowed in the section/subsection. This is signified by the <code>[]</code>. Ranges can be specified by a dash.

In the first subsection of our expression, we can see <code>[a-z0-9_\.-]</code>, which shows that any lowercase letter, number,_,.,or- can be accepted for validation. If any other characters are used, it will not pass validation.


### Character Classes
Character classes are indicators that can stand for other ranges, so that the expression can take up fewer characters. They are not necessary to use, but can make coding the expressions easier.
<code>.</code> can match with any character.
<code>\d</code> can match with numbers.
<code>\w</code> can match with any alphanumeric character and the underscore.
<code>\s</code> can match with a single whitespace character.

### The OR Operator
The OR operator is a <code>|</code> that signifies the word "or" in English. For instances <code>(a|b|c)</code> means that either a,b, or c can be accepted in the subsection.

### Flags
Are placed at the end of the expression after the second slash. Here are some of the flags that can be used:

<code>g</code> is a global search that says the expression should be tested against all possible matches in a string.

<code>i</code> makes the search case insensitive.

<code>m</code> means the string should be treated as multiple lines.

### Character Escapes
A Character Escape in a Regular Expression is a <code>\\</code>. It escapes a character that would signify something else in the expression to indicate that you actually wanted the character to be present. For instances <code>|</code> is an "or" operator, but <code>\\|</code> will show the actual character. To escape a backslash, simply use two backslashes <code>\\\\</code>.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

Thank you for reading my article.

Author: Hunter Steffner

To see more of what I am working on, please check out my github: [huntersteffner](https://github.com/huntersteffner)