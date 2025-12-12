---
tags: CMSC_250
created: 2025-12-4
description: 12/1, 12/3, 12/5, 12/8, 12/10 notes (Lecture 33, 34, 35, 36, 37)
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
> All elements must be related to itself.
> 
> **Irreflexive**: $(\forall a \in A) [a \cancel{R} a]$

> [!info] Symmetric
> **Symmetric**: $(\forall a, b \in A) [a R b \rightarrow b R a]$
> 
> **Antisymmetric**: $(\forall a, b \in A) [(a R b \land b R a) \rightarrow a = b]$

> [!info] Transitive
> **Transitive**: $(\forall a, b, c \in A) [(a R b \land b R c) \rightarrow a R c]$

> [!info] Total
> **Total**: $(\forall a, b \in A) [a R b \lor b R a]$
> 
> Any two elements in the set need to be related to each other

### Types of Binary Relations

> [!info] Equivalence Relation
> A binary relation is an **equivalence relation** if it is:
> - Reflexive
> - Symmetric
> - Transitive
> 
> An equivalence relation partition the domain into "equivalence classes."
> $$[a] = \{ x \in A | x R a \}$$

> [!info] Partial Order
> A binary relation is a **partial order** if it is:
> - Reflexive
> - *Antisymmetric*
> - Transitive
> 
> A partial order is when there are multiple "streams" that all "flow" in one direction, with no cycles.

> [!info] Total Order
> A binary relation is a **total order** if it is:
> - Total (which implies reflexive) (this means every element in the set must be related to one another)
> - Antisymmetric
> - Transitive
> 
> Essentially, a total order is a partial order that is also total.
> 
> A total order is sometimes called a "linear order" since it looks linear.

> [!info] Well Order
> A binary relation, $R$, is a **well order** over $S$ if:
> - It is a total order
> - Every non-empty subset of $S$ has a *least* element
> 
> A well order is linear with no infinite descending chains.

### Numbers representing "infinity"

##### Ordinals

**Ordinals** are numbers used to describe the *shape* of (really complex) *lists*..

The ordinals are used for indexing "lists" that go beyond just $N$.

Any well-ordering is "isomorphic" to one of the ordinals.

##### Cardinals

**Cardinals** are numbers used to measure the *size* of a *set*.

> [!info]
> If $f$ is one-to-one then $|A| \leq |B|$.
> 
> If $f$ is onto then $|A| \geq |B|$.
> 
> If $f : A \rightarrow B$ is a bijection then $|A| = |B|$.

$\aleph_0$ ("aleph-null") is the symbol used to denote the cardinality (size) of the natural numbers (so $|N| = \aleph_0$).

$\aleph_0$ is the smallest *infinite cardinal*. Any infinite set that has size $\aleph_0$ is said to be *countable*.

> [!info]
> Adding an element to an infinite set does not make it bigger.