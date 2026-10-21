---
tags: CMSC_330
created: 2026-10-20
description: 10/20 notes
---

### Compilers/Interpreters

**Compiler**: Convert from one language to machine code

**Practically**: Convert from language to Assembly

**Abstracted**: Convert from language to another

- Three things needed for a translator
	- **Lexer**: Typically use RE to convert text file to a list of tokens (word types)
	- **Parser**: Converts tokens to an Abstract Syntax Tree using a Context Free Grammar (CFG)
	- **Evaluator/Generator**: Converts AST to Target or evaluates to value

### Grammars

**Regular Expression (RE)**: Describes a string

**Context Free Grammars (CFGs)**: Describes a set of strings but more of them

**Grammar**: Structure of a language

- Things we need for  a CFG
	- $\Sigma$: Alphabet (known as terminals)
	- Non-Terminals: Denotes groups of terminals
	- Productions: Says what symbols can replace others
	- Start symbol: Where to start

> [!example]
> `/[01]+/` (want to generate "001")
> 
> $S \rightarrow 0S | 1S | 1 | 0$
> $S \Rightarrow 0S$
> $0S \Rightarrow 00S$
> $00S \Rightarrow 001$

Above process is called **deriving**.

> [!tip] Recursion in Grammars
> Recursion allows for repetition.
> 
> $S \Rightarrow 0S|\epsilon$

> [!tip] Concatenation in Grammars
> Separate non-terminals can be used for concatenation.
> 
> $S \rightarrow AB$
> $A \rightarrow \text{hello}$
> $B \rightarrow \text{world}$)

Unlike Regex, we can refer backwards. Start at middle of string and build outward.

> [!tip] Unions in Grammars
> Each path in a union can be a non-terminal.
> 
> `(c|k)l(i|y)(ff|ph)`
> 
> $S \rightarrow AlBC$
> $A \rightarrow c|k$
> $B \rightarrow i|y$
> $C \rightarrow ff|ph$

### Parse Trees and ASTs

Grammar describes structure of a language, and we can model this structure with a **parse tree**.

Sometimes multiple trees exist, where there are left and right derivations and they may have multiple derivations. This is **ambiguity**, which is bad.

- Two ways to fix ambiguous grammars
	- Rewrite it
	- Different parsers have different rules 

CFGs can describe programming languages.

An Abstract Syntax Tree (AST) is the backend data structure parsers use.

Parse trees show how things should be parsed, and ASTs are the abstraction of a parse tree.