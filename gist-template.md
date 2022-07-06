# Regex-maham

This is a Regex tutorial and a break down of a regular expression snippet. URL - 
```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

```



## Summary

explain here:
`^` Beginning. Matches the beginning of the string, or the beginnign of a line if the multiline flag (m) is enabled.
`(https?:\/\/)` Groups mutliple tokens together and create a capture group for extracting a substring or using a backreference.
`h` Character
`t` Character
`t` Character
`p` Character
`s` Character
`?` Qualifier
`:` Character
`\/` Escaped Character
`\/` Escaped Character

`([\da-z\.-]+)` Groups multiple tokens together and creates a capture group for extracting a substring or using a backreference.
`[]` Character set
`\d` Digit
`a-z` Range
`\.` Escaped Character
`-` Character
`+` Qualifier
`([a-z\.]{2,6})` Group 3 has multiple tokens together and creates a capture group for extracting a substring and using a backreference. 
`[]` Character set
`a-z` Range
`\.` Escaped Character
`{2,6}` Quantifier
`([\/\w \.-]*)` Group 4 has multiple tokens together and creates a cpature gorup fo extracting a substring of or using a backreference.
`[]` Character set 
`\/` Escaped Character
`\w` Word
`\.` Escaped Character
`-` Character 
`*` Qualifier
`\/` Escaped Character
`?`Quantifier
`$` End





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

`^` matches at the beginning of the target string
`$` matches at the end of the target string
`\` b matches on a word boundary

### Quantifiers

 `*`  representing 0 or more occurrences of the atom,
  `+` representing 1 or more occurrence of the atom,
 `?` representing 0 or 1 occurrences of the atom,
the bound {n}   representing exactly n occurrences of the atom,
the bound {m,n}   representing between m and n occurrences of the atom.





### OR Operator
To match patterns based on a specific character, follow the character with the operator `*` , `+` , or `?` . These operators indicate the number of times the character should occur for a match—zero or more, one or more, or one or zero, respectively. 

### Character Classes

`[ ... ]` 
With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters.
Simply place the characters you want to match between square brackets. If you want to match an a or an e, use `[ae]`. You could use this in gr`[ae]`y to match either gray or grey. Very useful if you do not know whether the document you are searching through is written in American or British English.


### Flags

`i` - With this flag the search is case-insensitive: no difference between A and a.
`g` - With this flag the search looks for all matches, without it – only the first match is returned.
`m` - Multiline mode
`s` - Enables “dotall” mode, that allows a dot . to match newline character `\` n.
`u` - Enables full Unicode support. The flag enables correct processing of surrogate pairs.
`y` - “Sticky” mode: searching at the exact position in the text.


### Grouping and Capturing

Capturing groups are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses.  For example, the regular expression (dog) creates a single group containing the letters "d" "o" and "g" .

### Bracket Expressions

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set.(an expression enclosed in square brackets, `"[]"` )

### Greedy and Lazy Match

For every position in the string try to match the pattern at that position but if there's no match, go to the next position. 
We have a text and need to replace all quotes `"..."` with guillemet marks: `«...»`. They are preferred for typography in many countries.





### Boundaries

Left - and Right -of - Word Boundaries: -The start of word boundary `[[:<:]]` is converted to `\b(?=\w)`
-The end of word boundary `[[:>:]]` is converted to `\b(?<=\w)`
Not-a-word boundary:` \B`
-`/B` matches all positions where /b doesnt match

The word boundary `\b` matches positions where one side is a word character (usually a letter, digit or underscore—but see below for variations across engines) and the other side is not a word character (for instance, it may be the beginning of the string or a space character)


### Back-references

Backreferences match the same text as previously matched by a capturing group.
To figure out the number of a particular backreference, scan the regular expression from left to right.By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag. Here’s how: `<([A-Z][A-Z0-9]*)\b[^>]*>.*?</\1>`. This regex contains only one pair of parentheses, which capture the string matched by `[A-Z][A-Z0-9]*`.

### Look-ahead and Look-behind

Lookahead and lookbehind, collectively called “lookaround”, are zero-length assertions 

## Author
Github [FogleA10](https://github.com/FogleA10)



