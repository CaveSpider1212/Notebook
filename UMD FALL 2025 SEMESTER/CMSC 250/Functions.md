---
tags: CMSC_250
created: 2025-11-24
description: 11/24 notes (Lecture 32, video lectures)
---

### Functions

A **function** assigns members of one set (the **domain**) to members of another set (**co-domain**).

The **range** is the subset of the co-domain that gets "hit" by elements of the domain.

A member of the domain can  only be assigned to *one* member of the co-domain.

> [!info] Notation
> Let $A = \{ 1, 2, 3 \}$ and $B = \{ 4, 8, 12 \}$.
> 
> Ways to express functions:
> - $f : A \rightarrow B$ such that for all $a \in A$, $f(a) = 4a$
> - $f : A \rightarrow B$ such that $a \mapsto 4a$
> - $f = \{ (1, 4), (2, 8), (3, 12) \}$

### Total vs. Partial

A **total function** assigns *every* member of the domain to an element of the co-domain.

A **partial function** may not assign every member of the domain.

### Injective Function

A function is **one-to-one** or **injective** if every element of the range is associated with *exactly* one element from the domain (meaning there cannot be any elements in the co-domain with more than 1 element of the domain mapping to it).

### Surjective Function

A function is **onto** or **surjective** if the range is equal to the entire co-domain (meaning every element in the co-domain has an element in the domain mapping to it, even if there are multiple elements mapping to it).

### Bijective Function

A function is **bijective** if it is both injective (one-to-one) and surjective (onto).

Sometimes called a "one to one correspondence."

### Inverse Image

Let $y$ be an element of the co-domain of a function.

The **inverse image** of $y$ is the subset of the domain that maps to $y$.

### Inverse Function

Let $f$ be a function. The **inverse** of $f$, denoted $f^{-1}$, is a function that "reverses" $f$.

> [!example]
> If $f(7) = \text{aardvark}$, then $f^{-1} (\text{aardvark}) = 7$.

Not all functions have inverses.

A function cannot have an inverse function if it isn't one to one.

If a function is one-to-one but not onto, then an inverse function does exist but it's a partial function.

A bijective function does have a total inverse function.

### Proving that a function is/isn't injective

> [!info] Injective Function Proofs
> Let: $f : D \rightarrow C$ such that...
> 
> Claim: $f$ is one-to-one.
> 
> Proof: Let $a, b \in D$.
> Assume $f(a) = f(b)$. \[I must show $a = b$.]
> ...
> $a = b$
> 
> Claim: $f$ is not one-to-one.
> 
> Proof: \[Find two different elements of the domain that are mapped to the same value.]