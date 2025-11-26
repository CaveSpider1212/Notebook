---
tags: CMSC_250
created: 2025-11-3
description: 10/31, 11/3, 11/5 notes (Lectures 23, 24, 25)
---

Examples: $A = {1, 2, 3}$ or $B = {x \in Z | -4 < x < 4}$

Sets do not allow "repetition," meaning an element is either in the set or not in the set.

### Set Concepts

- The symbol $\in$ means "is an element of"
- The symbol $\notin$ means "is not an element of"
- $n(S)$ or $|S|$ represent the **cardinality** of $S$, which is the number of elements in $S$
- A set can be finite or infinite
- The universal set ($U$) is the set consisting of all possible elements that are under consideration

### Subset

$A \subseteq B$ means: $(\forall x \in U) [x \in A \rightarrow x \in B]$

- "Every element of $A$ is also an element of $B$"
- "$A$ is a subset of $B$"
- Note: "$A \subseteq B$" is NOT the same as "$A \in B$"
- Avoid saying "contains"

> [!info] Definition of Subset
> $$(A \subseteq B \land x \in A) \rightarrow x \in B$$

Proper subset: $A \subset B$ means $A \subseteq B \land A \neq B$

### Set Operations

> [!info] Definition of Union
> $A \cup B = {x \in U | x \in A \lor x \in B}$
> 
> Joining sets $A$ and $B$ (the union set contains all elements in $A$ or $B$)

> [!info] Definition of Intersection
> $A \cap B = {x \in U | x \in A \land x \in B}$
> 
> Finding elements that are in both sets $A$ and $B$

> [!info] Definition of Complement
> $A^c = A' = \bar{A} = {x \in U | x \notin A}$
> 
> All elements not in set $A$

> [!info] Definition of Difference
> $A - B = {x \in U | x \in A \land x \notin B}$
> 
> Elements in set $A$ but not in set $B$

### Empty Set

The empty set $\emptyset$ has no elements, so $\emptyset = \{ \}$.

1. For any set $X$: $[\emptyset \subseteq X]$
2. For any set $X$: $[X \cup \emptyset = X]$
3. For any set $X$: $[X \cap \emptyset = \emptyset]$
4. For any set $X$: $[X \cap X' = \emptyset]$
5. $U' = \emptyset$
6. $\emptyset' = U$

### Disjoint Sets

If $A$ and $B$ were disjoint, then $A$ and $B$ have no elements in common and $A \cap B = \emptyset$. ^29cfda

### Ordered n-tuples

$$(x_1, x_2, x_3, ..., x_n)$$

This is like a list, not a set.
Repeats are allowed, and order matters

### The Cartesian Product

The Cartesian product of sets $A$ and $B$ is defined as

$$A \times B = {(a, b) | a \in A \land b \in B}$$

$n(A \times B) = n(A) \times n(B)$

### Proving Subset Relationships

> [!info] Subset Relationship Proof
> Claim: $A \subseteq B$
> 
> Proof: Let $x \in A$. \[It suffices to show $x \in B$]
> ...
> $\therefore x \in B$

The above proof also frequently resembles the following proof:
> [!info] Subset Relationship Alternative Proof
> Claim: $A \subseteq B$
> 
> Proof:
> $x \in A \rightarrow S1$
> $\hspace{13.5mm} \rightarrow S2$
> $\hspace{13.5mm} \rightarrow S3$
> $\hspace{13.5mm} ...$
> $\hspace{13.5mm} \rightarrow x \in B$

### Proving Set Equality

> [!info] Set Equality Proof (Technique #1)
> Claim: $A = B$.
> 
> Proof:
> $x \in A \leftrightarrow \text{S1}$
> $\hspace{13.5mm} \leftrightarrow \text{S2}$
> $\hspace{13.5mm} \leftrightarrow \text{S3}$
> $\hspace{13.5mm} ...$
> $\hspace{13.5mm} \leftrightarrow x \in B$

Note: $A = B \leftrightarrow A \subseteq B \land B \subseteq A$

> [!info] Set Equality Proof (Technique #2)
> Claim: $A = B$.
> 
> Proof:
> Part I. \[Show $A \subseteq B$]
> ...
> Part II. \[Show $B \subseteq A$]
> ...

It is a good idea to use [[Proofs#^6578a5|proof by contradiction]] when dealing with empty sets and equality, meaning if we were to prove $A = \emptyset$, we would start off by saying $x \in A$ by way of contradiction.

### Powersets

$P(A)$ is the set of **all** subsets of $A$

Note: $n(P(X)) = 2^x$ (giving us the size of the powerset), where $x$ is the size of the set $X$.

> [!example]
> $P(\{ a, b, c \}) = \{ \emptyset, \{ a \}, \{ b \}, \{ c \}, \{ a, b \}, \{ a, c \}, \{ b, c \}, \{ a, b, c \} \}$
> 
> $P(\emptyset) = \{ \emptyset \}$
> 
> $P(\{ \emptyset \}) = \{ \emptyset, \{\emptyset \} \}$

> [!info] Definition of Powerset
> $$A \subseteq B \leftrightarrow A \in P(B)$$