---
tags: CMSC_250
created: 2025-9-14
description: 9/12, 9/15, 9/17 notes (Lectures 5, 6, 7, and 8)
---

> [!info] Predicate
> Predicates are boolean expressions containing variables.
> 
> They can be either true or false depending on the value assigned to the variable.
> 
> Example: P(x) = "x is even"

Logical connectives can be used to join predicates to make more complex predicates.

> [!tip] Universal Quantifier ($\forall$)
> This shows that a predicate works for all values of the variable in the domain.
> 
> $$(\forall x \in D) [P(x)]$$

> [!tip] Existential Quantifier ($\exists$)
> This shows that there exists a variable in the domain such that the predicate is true.
> 
> $$(\exists x \in D) [P(x)]$$

Negation: Move the negation sign inside with the predicate and flip the quantifier
$\sim (\forall x)[L(x)] \equiv (\exists  x)[\sim L(x)]$
$\sim(\exists x) [F(x)] \equiv (\forall x)[\sim F(x)]$

### Nested Quantifiers

Examples:
- $(\forall x \in D) (\exists y \in D) [S(x, y)]$ --> "For all $x$ in $D$, there exists a $y$ in $D$ such that $S(x, y)$ holds"
- $(\exists x \in D) (\forall y \in D) [T(x, y)]$ --> "There exists an $x$ in $D$ for all $y$ in $D$ such that $T(x, y)$ holds"

Negation: Move the negation sign inside with the predicate and flip each quantifier
$\sim(\forall x)(\exists y)[Q(x, y)] \equiv (\exists x) \sim(\exists y) [Q(x, y)] \equiv (\exists x)(\forall y)[\sim Q(x, y)]$

### Translating English to First Order Logic

> [!example]
> Let $C =$ {Creatures on Earth}
> Let $B(x) =$ "$x$ is a Bear", where $x \in C$
> 
> - There is at least one Bear: $(\exists x)[B(x)]$
> - There are no Bears: $\sim(\exists x)[B(x)] \equiv (\forall x)[\sim B(x)]$ <--- "For all creatures on Earth, they are not Bears"
> - There is at most one Bear: $(\forall x, y)[(B(x) \land B(y)) \rightarrow (x = y)]$ <--- "For all Creatures $x$ on Earth, if $x$ is a Bear and $y$ is a Bear then they are both the same Bear"
> - There is exactly one Bear: $(\exists x)[B(x) \land (\forall y)[B(y) \rightarrow x = y]]$ <--- "There exists a Creature $x$ such that $x$ is a Bear and for all Creatures $y$, if $y$ is a Bear then $y$ and $x$ are the same Bear"
> - There are at least two Bears: $(\exists x)(\exists y)[B(x) \land B(y) \land x \neq y]$ <--- "There exists a Creature $x$ and a Creature $y$ such that $x$ and $y$ are both Bears and are not the same Bear"

### Free vs. Bound Variables

Free variables are not bound by quantifiers (statements can't have these).

Bound variables are.

### Interpretations of Statements

> [!info] Interpretations
> An "interpretation" of a statement is:
> 1. A choice of domain(s)
> 2. An assignment of meaning to the predicate symbol(s)

> [!example]
> $P(a, b)$ means "$a + b = 0$"
> $P(a, b)$ also means "$a$ is the additive inverse of $b$"
> $(\forall a)(\exists b)[P(a, b)]$ means "Every number has an additive inverse"
> 
> True for $R$ and $Z$, false for $N$