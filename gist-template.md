# Regular Expressions Tutorial

Regular expressions, also known as Regex, are special characters that define a search pattern.

## Summary

In this tutorial I will explain the usage of the component of the selected regular expresssion.

Regular expressions can feel like their own language at times, but in fact they are universal and can be used within all programming languages. Let's break down the preceding “Matching a Hex Value" regex in order to explore regex components in general.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)

## Regex Components

### Anchors

The regex I selected uses two anchors, ^ and $ :

- The ^ anchor means that the string begins with the character that follows it. In this case the starting character is #.

- The $ anchor means a string that ends with the characters that precede it.

### Quantifiers

Quantifiers are the last requirements of the regex. They set the limits of the string. The regex we selected has the following quantifiers:

- The ? matches the pattern zero or one time.

- The {6} matches the pattern exactly 6 times, this represents the length of the component.

- The {3} matches the pattern exactly 3 times, this also represents the length of the component. We have two length components because we have two types of formats, and we know this because of the or operator, which will be explained later.

### Grouping Constructs

Grouping constructs break the different sections with () in the regex. They have two primary categories:

- Capturing groups capture the matched character sequences for possible re-use (including a numbered backreference) while non-capturing groups do not. 

A grouping construct can be made non-capturing by adding the characters ?: at the beginning of an expression inside the parentheses.

### Bracket Expressions

Anything inside a set of square brackets ([]) represents a range of characters that we want our regex to match. Our expression has the following characters:

- [a-f0-9] and [a-f0-9], looking for a lowercase letter included in the a to f range and for a number included in the range 0 to 9.

### Character Classes

The character classes define a set of characters that we are expecting to match. In our case we are using character classes defined by the [] symbols. Our regex has two character classes: [a-f0-9] and [a-f0-9]

### The OR Operator

The OR Operator is represented by the | character. This operator indicates that it could be one or the other of the two components we are separating with the | symbol. The selected regex has to types of formats, that is why we are using the OR operator. This means that our first pattern can either be 6 characters [a-f0-9]{6} or 3 characters [a-f0-9]{3}.

## Author

This tutorial was put together by Sandra Mendoza as part of the full-stack web developer bootcamp. My GitHub:  https://github.com/sandraxmm

