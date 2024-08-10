# Regex-Tutorial

What in the world is Regex?! Well, let me tell you what I have learned about it.  

## Summary

Regex is a short for regular express, which uses a series of characters to recognize patterns in user input. The most common occurance of using regex is when signing up for a service or filling out a form to verify that you are entering your information correctly. For example, when entering your email address, at the bottom it may say something along the lines of please enter a your email (i.e. youremail@email.com). If what the user entered doesn't follow this pattern then it will give you an error. 

```bash
const regexEmail = ^\w*(\-\w)?(\.\w*)?@\w*(-\w*)?\.\w{2,3}(\.\w{2,3})?$;
```

There's a lot going on there, lets break it down!

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

### Anchors

Like most things in life, there is a beginning and an end. Regex uses a caret ( ^ ) to match beginning of a string and dollar sign ( $ ) to match the end. 

### Quantifiers

Quantifiers are used to specify the number of characters.

| Quantifiers | Definition of use |
|:---:|:---|
|n+| Matches "n" at least once or more. ("nevah") |
|n*| Matches "n" 0 or more times. (/ne*/ in "neeeeeevah" and "necturine") |
|n?| Matches string that contains 0 or 1 "n". (/ev?e?/ matches "nevah" and "very")|
|n{M}| Matches a specific number of "n". (/n{3}/ matches "nnnevah" but not "nnevah". However will match with "nnnnnnnevah" but only the first three "n"s.) |
|n{M,}| Matches a specific number of "n". Similiar to the previous quntifier (/n{3}/ does  not match "nnevah". The main difference is that it will match "nnnevah" and all the "n"s in "nnnnnnnevah") |
|n{M,E}| Matches between the range of "M" and "E". (/n{1,3}/ matches with "nevah", "nnnevah", and nnnnnevah" however will only match the 3 "n"s. ) |
|n$| Matches inputs that end with "n". (/n$/ matches with haven.) |
|^n| Matches with inputs that start with "n". (/^n/ matches with "nevah") |

### Grouping Constructs

Groupings in regex are found inside of parentheses(), they are a great way to simplify a complex pattern. 
(abc) will match with the exactly with "abc"
(ab|ba) will match "ab" or "ba".

### Bracket Expressions

Bracketts are used to specifiy a range of character. 
Example: [a-z]  [0-9]

### Character Classes

Metacharacters are used to write regex patterns in a more compact way, that way your code isn't 1,000 ccharacters long. Each class matches a set of characters, digits, and whitespaces.
There are many more metacharacters, checkout <a href="https://www.w3schools.com/jsref/jsref_obj_regexp.asp">W3schools</a> list of metacharacters and their meanings.

| Metacharacters Class | Definition of use |
|:---:|:---|
|\s| Match whitespace characters (space and tab) |
|\t| Match only the tab character |
|\d| Match digit characters (numbers) |
|\w| Match any work characters (alphanumeric and underscores_) |
|\b| Match word boundary (spaces , - ; :) |


### The OR Operator

### Flags

Flags are used like filters, you can apply one or have multiple. They add an extra funtionality to your search just as global search and case- insensitivity.

|Flag| Definition of use |
|:---:|:---|
|d| Match should contain indices of the dubstring of each capture group |
|g| Global search|
|i| Case-insensitive search |
|m| Mlitiline mode using anchors "^" and "$"  |
|s| "dotall" mode, uses a dot "." to match newline character |
|u| Unicode support |
|v| Unicode support plus more features |
|y| "sticky" search, matches from the current position of the target string |

### Character Escapes

Sometimes you want to search for the actual character that is used in regex, in order to make that work you need to escape  by putting a backslash "\" in front of the character. For example, in order to search for "/nevah/" but its followed by more characters you would do the following. 

```bash
/\/nevah\/[a-z]+/i
```

## Author

You can find more of my works and projects on my <a href='https://github.com/nevah-evans'>Github</a>!