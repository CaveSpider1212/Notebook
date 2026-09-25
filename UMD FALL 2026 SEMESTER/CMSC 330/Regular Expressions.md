---
tags: CMSC_330
created: 2026-9-24
description: 9/24 notes
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