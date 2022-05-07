# Regex Tutorial

Regular expression or Regex for short, is used for the purpose of allowing a computer to search for a character or set of characters though search string algorithms. In order to write code in Regex a particular syntax must be followed. The purpose of this tutorial is to assist developers in writing syntax in Regex to be used in their applications.

## Summary

This tutorial will include many of the common Regex components. However, it does not cover every component available in Regex. Additionally the components introduced in this tutorial include the most common uses of the component in question. However, advanced users are capable of more complex searches using the components described in this tutorial.

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

When a simple string is searched using Regex the application will search for any instance of the string. This includes instances where the string is small part of a larger string.  
Example: Searching the string "not" would result in not just the word "not" but also words such as "cannot" "notification" or "hypnotherapy".

Should a user have a need to find the strong "not", the anchors ^ and $ would need to be included.  
Example: Searching ^not$ would yield only the word "not" and exclude any other words that included the characters n, o, and t.

The anchors can also be use individually. If only the ^ anchor is use then the results would yield strings with that start with the desired string. On the other hand if the $ anchor is used then the results would yield strings that end with the desired string.
Example: Searching ^not would yield results "not" or "notification". Searching not$ would yield search results such as "not" or "pinot".

### Quantifiers

Quantifiers are the special search characters _ + ? and {} which specify how many identical string characters must follow a given string.  
In the example xyz consider the following uses and search results:
Searching xyz_ yields xy immediately followed by zero or more z characters.
Searching xyz+ yields xy immediately followed by one or more z characters.
Searching xyz? yields xy immediately followed by zero or one z characters.
Searching xyz{a} yields xy immediately followed by an a amount of z characters.
Searching xyz{a, } yields xy immediately followed by an a amount or more z characters.
Searching xyz{a, b} yields xy immediately followed by an a amount up to b amount of of z characters.

### OR Operator

The OR operator specified by the character | searches for a string that follows one of two specified characters.
Example: Searching x(y|z) would yield a result where the character x would be followed by either the character y or z.

### Character Classes

Characters classes are searched using \d \s \w or . See the samples below for it's uses.
\d would match a character that is a digit.
\s would match white spaces including tabs and line breaks.
\w would match alphanumeric characters
. would match any character

### Flags

Some Regex flags include the search characters g for global, u for unicode, and i for case sensitive.
In the case of the global flag when included it results in all instances of the search sting to be included not just the first instance.
In the unicode flag allows for searches to include unicode.
Using the i flag allows for the search to be case sensitive.

### Grouping and Capturing

Grouping and Capturing are used using ( ) characters. When these search characters are used they allow for the search to yield results within a string.

### Bracket Expressions

Bracket Expressions indicated by the use of the [ ] characters. Allow for a shorthand version of the OR component.  
Example: 1|2|3|4|5 could be instead searched by doing [12345]

### Greedy and Lazy Match

Greedy searches specified by <.+> will search for instances as much as possible.  
Lazy searches specified by adding a ? after the + (example: <.+?>) will repeat the search as few times as possible.

### Boundaries

Boundaries specified by adding /b to both ends of the search sting allow for searches to begin with a world but ends with non-words.

### Back-references

Back-references are components indicated by a / immediately followed by a number. This component identifies the search string followed by a second, third, fourth, or so depending on the value of the number used in the back-reference.

### Look-ahead and Look-behind

These components indicated by the characters (?=) and (?<=) are used to search for strings that are either preceding or succeed a given string.  
Example: 1(?=2) would only yield results that have a 1 that is preceding a 2. Where as (?<=2)1 would yield results where as a 1 succeeds a 2.

## Author

This tutorial was created by Christopher Palileo
[GitHub](https://github.com/cpalileo)
