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

### Bracket Expressions

### Character Classes

<strong>Metacharacters</strong> are used to write regex patterns in a more compact way, that way your code isn't 1,000 ccharacters long. Each class matches a set of characters, digits, and whitespaces.
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

### Character Escapes

## Author

You can find more of my works and projects on my <a href='https://github.com/nevah-evans'>Github</a>!