# Regex

### Character Classes I

| Symbol/Expression | Meaning |
|---|------|
|\d | Match a digit character |
|\D | Match a non-digit character |
|\s | Match a single white space character (space, tab, form feed, or line feed) |
|\S | Match a single character other than white space|
|\w | Match any alphanumeric character (including underscore) |
|\W | Match any non-word character |

### Character Classes II

| Symbol/Expression | Meaning |
|---|------|
|[abc] | Match any one of the characters in the set 'abc' |
|[^abc] | Match anything not in character set 'abc' |
|[\b] | Match a backspace |

### Assertions

| Symbol/Expression | Meaning |
|---|------|
|^ | Match beginning of input |
|$ | Match end of input |
|\b| Match a word boundary |
|\B| Match a non-word boundary |

### Alternations

Works as an 'OR' operator; the symbol is ```|```.

### Capturing Group

Defined by the usage of parentheses; the symbol is ```()```.

<br>

***

## Summary & Caveats

- ^ marks the start of the line;
- $ marks the end of the line;
- There are 3 types of metacharacters:
  - Has metacharacter meaning only <u>outside</u> the character class, ex: ```()```;
  - Has metacharacter meaning only <u>inside</u> the character class, ex: ```-```;
  - Has metacharacter meaning <u>both inside and outside</u> the character class, but the meaning is different, ex: ```^```;
- (a|b|c) means the same as [abc] but a generic use case doesn't hold. A character class matches exactly one character, while alternation can match as many characters as you define;
- A negated char class [^x] doesn't mean "match unless there is an x";
- Use shorthands like \s, \S, \d, \D, \w, \W to shrink your regex.

<br>

<br>

**Source:** https://www.udemy.com/course/practical-regex/
