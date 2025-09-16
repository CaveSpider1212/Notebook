---
tags: CMSC_250
created: 2025-9-14
description: 9/12, 9/15 notes
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