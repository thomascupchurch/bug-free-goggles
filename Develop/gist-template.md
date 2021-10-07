# 'img-src' Regex Tutorial

Welcome to the regex tutorial for img-src. I hope you find this helpful.

## Summary

The img-src regex matches the source (src) of an image (img) tag in html. Useful when searching for image code within a larger document, one could use this to cut down on time looking through html code to find the source for problematic image links. Before we do anything else, this is the regex:

/^<\s*img[^>]+src\s*=\s*(["'])(.*?)\1[^>]\*>$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Back-references](#back-references)(#look-ahead-and-look-behind)

## Regex Components

The img-src regex is composed of the following:

`^<` which requires the pattern to begin with an opening angle bracket;

`\s` which allows whitespace to immediately follow the opening `<`;

`*` which refers to the previous whitespace allower and expands it to allow for 0 or more whitespaces;

`img` which searches for the html image tag pattern of `i`, followed by `m`, followed by `g`;

`[^>]` which excludes a closing angle bracket from immediately following the opening `<img`;

`+` which refers back to the excluded closing angle bracket and expands its meaning to include 1 or more;

`src` which searches for the pattern of `s`, followed by `r`, followed by `c`, to signify the `src` syntax in an html img element;

`\s*` which allows for zero or more whitespaces;

`=` which is standard in the img src syntax in html;

`\s*` again allows for zero or more whitespaces;

`(["'])` searches for use of either single or double quotes;

`(.*?)` searches for zero or more dots, with the `?` making the search "lazy" so as to match as few characters as possible;

`\1` references capture croup number one, which was `(["'])`, and thus matches for closing single or double quotes, as is required in the img element src syntax;

`[^>]*` allows for 0 or more of any character other than a `>` closing angle bracket (e.g. a closing `/` slash, which is not required but may be present);

`>` matches a required closing angle bracket;

`$` signifies that the string must end here, immediately following that preceding closing angle bracket.

### Anchors

Uses beginning anchor, `^`, and end anchor, `$`

### Quantifiers

Uses the one-or-more plus quantifier, `+`; the zero-or-more star, `*`; and the lazy, `?`, causing the preceding quantifier to match as few characters as possible.

### Character Classes

Uses word, `\w`; whitespace, `\s`; dot, `.`;

### Grouping and Capturing

Uses two capturing groups, `(["'])` and `(.*?)`.

### Greedy and Lazy Match

Uses the lazy to match as few dots at possible.

### Back-references

Uses numeric reference, `\1` to refer back to the first capture group.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
