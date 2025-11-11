---
tags: CMSC_250
created: 2025-11-5
description: 11/5, 11/7, 11/10 notes (Lecture 25, 26, 27)
---

### Probability

**Probability** is how likely something is to happen.

Goes from 0 (smallest possible) to 1 (largest possible)

Expressed as fractions, decimals, percentage, or "1 in $x$" (for small values)

### Partitions of a Set

A collection of *nonempty* sets ${A_1, A_2, ..., A_n}$ is a **partition** of the set $A$ if and only if:
1. $A = A_1 \cup A_2 \cup ... \cup A_n$
2. $A_1, A_2, ..., A_n$ are mutually [[Set Theory#^29cfda|disjoint]]

An infinite set can also be partitioned, and the partition can be finite or infinite.

### Classical Probability Formula

Definitions:
- **Sample Space** (S): Set of all possible outcomes
- **Event** (E): Any subset of the sample space

> [!info] Classical Probability Formula
> If we have a Sample Space, S, *where every element of the sample space is equally likely*, then the probability of an event, E, is given by:
> 
> $$P(E) = \frac{n(E)}{n(S)}$$

### Multiplication Rule of Counting

> [!info] Multiplication Rule of Counting
> $$n_1 \times n_2 \times ... \times n_K$$
> 
> (where $n_i$ is the number of ways to perform step $i$)

### Independent Events

Two events are said to be "**independent**" if the occurrence of one event does not effect the probability of the other event.

> [!info] Multiplication Rule for Independent Events
> Assume that events $E_1, E_2, E_3, ..., E_k$ are *all mutually independent*. Then:
> 
> $$P(E_1 \cap E_2 \cap E_3 \cap ... \cap E_k) = P(E_1) \times P(E_2) \times P(E_3) \times ... \times P(E_k)$$
> 
> Note: This is the same as saying "$E_1$ and $E_2$ and $E_3$ and ... and $E_k$"

### Probabilities of Complements

$E^c$ is the event "$E$ does NOT happen" (the complement).

$$P(E^c) = 1 - P(E)$$

### Mutually Exclusive Events

Two events are said to be "**mutually exclusive**" if they cannot happen at the same time (meaning if one occurs, the other is impossible).

> [!info] Addition Rule for Mutually Exclusive Events
> If $E_1, E_2, E_3, ..., E_k$ are *mutually exclusive*, then:
> 
> $$P(E_1 \cup E_2 \cup E_3 \cup ... \cup E_k) = P(E_1) + P(E_2) + P(E_3) + ... + P(E_k)$$
> 
> Note: This is the same as saying "$E_1$ or $E_2$ or $E_3$ or ... or $E_k$"

When doing problems with events using the Addition Rule, we can solve it by either partitioning the event (as disjoint subsets) or as "steps in a process."

### Inclusion-Exclusion Principle

> [!info] Inclusion-Exclusion Principle
> If there are two sets/events, then:
> 
> $$n(A \cup B) = n(A) + n(B) - n(A \cap B)$$
> $$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$
> 
> Note: Applies to [[Set Theory|sets]] as well