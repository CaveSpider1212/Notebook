---
tags: CMSC_250
created: 2025-11-5
description: 11/5 notes (Lecture 25)
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

Two events are said to be "independent" if the occurrence of one event does not effect the probability of the other event.