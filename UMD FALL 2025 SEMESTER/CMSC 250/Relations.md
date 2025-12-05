---
tags: CMSC_250
created: 2025-12-4
description: 12/1, 12/3 notes (Lecture 33, 34)
---

### Pigeon Hole Principle

A function from a finite set to a *smaller* finite set *cannot be one-to-one*.

> [!info] Generalized Pigeon Hole Principle
> If $N$ objects are placed into $k$ boxes, at least one box must contain $\lceil \frac{N}{k} \rceil$ objects.

### Relations

A **relation** among sets is a *subset* of their [[Set Theory#^83f6dd|Cartesian product]].

Relations can involve any number of sets, but most frequently they are **binary** (two sets).

### Binary Relations vs. Predicaates

A **binary relation** is a *set* (such as $R = \{ (\text{bear}, \text{acorn}, (\text{bear}, \text{fish}), (\text{squirrel}, \text{acorn}), (\text{whale}, \text{fish}), (\text{whale}, \text{plankton}) \}$).

A **predicate** is a Boolean expression (see [[Intro to First Order Logic#^8581ba]]).

They are essentially the same idea: $(a, b) \in R \leftrightarrow P(a, b)$.

> [!info] Predicate Notation for Binary Relations
> $$(a, b) \in R \leftrightarrow R(a, b) \leftrightarrow a R b$$

### Functions as Binary Relations

Any function can be thought of as a binary relation.

> Let $f : A \rightarrow B$ be a function.
> We can define relation $R$ as $\{ (a, b) \in A \times B : f(a) = b \}$.

### n-ary Relations

Relations can involve any number of sets (unary, binary, ternary, etc.).

> [!example]
> $R^n = (R \times R \times R \times ... \times R)$
> 
> Define relation $R \subseteq R^n$ as:
> $(x_1, x_2, x_3, ..., x_n) \in R$ if and only if $\sqrt{x_1^2 + x_2^2 + x_3^2 + ... + x_n^2} \leq 1$.

### Properties of Binary Relations

> [!info] Reflexive
> **Reflexive**: $(\forall a \in A) [a R a]$
> 
> **Irreflexive**: $(\forall a \in A) [a R a]$

> [!info] Symmetric
> **Symmetric**: $(\forall a, b \in A) [a R b \rightarrow b R a]$
> 
> **Antisymmetric**: $(\forall a, b \in A) [(a R b \land b R a) \rightarrow a = b]$

> [!info] Transitive
> **Transitive**: $(\forall a, b, c \in A) [(a R b \land b R c) \rightarrow a R c]$