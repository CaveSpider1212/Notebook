---
tags: CMSC_330
created: 2026-9-24
description: 9/24, 9/29 notes
---

### Regular Expressions (RegEx)

- Concatenation (/)
	- "hi" = "h" `concat` "i"
	- Take multiple regular expressions and concatenate them into one string in a set
- Union (|)
	- $\{ \text{"hello"} \} \cup \{ \text{hi} \} = \{ \text{"hello"}, \text{"hi"} \}$
	- Takes multiple regular expressions and joins them in a single set
- Repetition
	- $a^*$
	- Called the **Kleene star**

> [!example] Concatenation
> /a/ = {"a"}
> /ab/ = {"ab"}
> /hello/ = {"hello"}

> [!example] Union
> /ab|hi/ = {"ab", "hi"}

Can also use parentheses for order of operations

/a(b|h)i/ = {"abi", "ahi"}

> [!example] Kleene Star
> /a*/ = {"", "a", "aa", "aaa", ....}

### Other Regular Expressions

> [!info] Sets
> In a set (like `[abc]`), one character is accepted out of the given chocies.
> 
> Accept a, b, or c in the example.

> [!info] Ranges
> Use a dash (-) for ranges, like `[a-z]`.
> 
> Accepts any lowercase letter (a-z) in the example.
> 
> If there are no parentheses, elements around the dash takes precedence.

> [!info] Negation
> Use a caret (^) for negation, like `[^0-9]`.
> 
> Above example matches with any character that is not a digit.

> [!info] Repetition
> `a*`: Match with 0 or more a's
> `a+`: Match with at least 1 a
> `a?`: Match with 0 or 1 a's
> `a{3}`: Match with exactly 3 a's
> `a{4, 5, 6}`: Match with 4, 5, or 6 a's
> `a{4,}`: Match with at least 4 a's
> `a{,4}`: Match with at most 4 a's

> [!info] Pattern
> Beginning of a pattern: `^`
> End of a pattern: `$`
> 
> Examples: 
> `^hello` matches with "hellocliff" but not "cliffhello"
> `$bye` matches with cliffbye but not byecliff
> `^hello$` matches with "hello" and nothing else
> `^(hi|bye)$` matches with "hi" and "bye" only
> `^hi|bye$` matched with "hi" and "bye" and other things starting with "hi" or ending with "bye"

> [!info] Wildcard
> Use a `.` to match with any single character.
> 
> Use `\.` to use a literal `.`