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
> If there are two events that are independent of each other, then, if one or the other were to happen at the same time:
> 
> $$n(A \cup B) = n(A) + n(B) - n(A \cap B)$$
> $$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$
> 
> Note: Applies to [[Set Theory|sets]] as well

### Probability Trees

Each branch in a **decision tree** leads to a possible event in the step (the whole tree represents a sequence of steps), and each branch from each of those events leads to the possible events given the previous event, and so on.

The number of leaves in the tree is the number of possible scenarios (or ways to arrange the events).

A **probability tree** is similar but also involves probabilities, and we need to multiply the probabilities of the individual events in the sequence of steps to get the probability of a leaf (which is an individual scenario, see above).

### Permutations of a List

The different ways of ordering objects in a list are called **permutations**.

> [!info] Permutations Formula
> The number of permutations of $n$ objects is $n!$.

> [!example]
> There are 18 kids in a Kindergarten class.
> 
> 1. How many ways are there for the kids to line up in front of the door?
> 2. If they line up randomly, what is the probability that Kevin is *not* next to Stacy?
> 
> This is a permutation since we want to know the different number of ways or order the kids in line. There are 18 kids, so there are $18!$ ways to line them up.
> 
> There are 17 ways for Kevin to be ahead of Stacy, and another 17 ways for Kevin to be behind Stacy. In addition, there are $16!$ ways to order the remaining kids. The probability that Kevin is next to Stacy is $\frac{2 \times 17 \times 16!}{18!} = \frac{1}{9}$. The complement of this (which is what the question is asking) would be $1 - \frac{1}{9}$.

### Selecting $r$ things from a set of $n$ things

##### Tuples (Lists)

In lists or "tuples," *repeats are allowed* and *order does matter*. For example $(R, G, G)$ and $(G, R, G)$ can both be in the set of tuples since order matters (so they are distinct elements).

> [!info] Formula for Tuples
> The number of ways to select an $r$-tuple from a set of size $n$ is $n^r$.

> [!example]
> Your calendar for April has 30 days. You will fill in each day with exactly one activity from this set: {study, work out, sleep in, clean the house}
> 
> 1. How many ways are there to complete the calendar?
> 2. What is the probability that you don't study on any of the days?
> 
> In this problem, we want to choose 30 things from a set of 4 items. In addition, repeats are allowed and order DOES matter, so this is a list. The number of ways to complete the calendar is the same as the number of ways to select a 4-tuple from a set of size 30, which is $4^{30}$.
> 
> Each day, if you don't study, then there are 3 possibilities out of 4 that you could add to the calendar if you are not studying, and this continues for all 30 days, so $n(E) = 3^{30}$. The probability would be $\frac{3^{30}}{4^{30}} = (\frac{3}{4})^{30}$.

##### R-Permutations

In "R-Permutations" (lists without repeats), there are *no repeats allowed* and *order does matter*. For example, $(G, Y, B)$ and $(G, B, Y)$ can be in the list since order does not matter (so they are distinct elements), but $(R, R, G)$ cannot be in the list since it has repeating elements.

> [!info] Formula for R-Permutations
> $$P(n, r) = \frac{n!}{(n - r)!}$$

> [!example]
> You own 60 unique paintings, but you only have room on the wall to put 6 of them in a row.
> 
> 1. How many ways are there for you to place 6 of your 60 paintings on the wall?
> 2. If you place the paintings randomly, what is the probability that your 6 favorites just happen to be selected?
> 
> In this problem, we are selecting 6 items from a set of 60. Repeats are not allowed and order DOES matter ("in a row"), so the number of ways there are to place 6 of the 60 paintings on the wall is $P(60, 6) = \frac{60!}{54!}$.
> 
> There are 6 favorites, and we want to know how many ways they can be ordered (which is a permutation), so $n(E) = 6 \times 5 \times 4 \times 3 \times 2 \times 1 = 6!$. Therefore, the probability would be $\frac{6! \times 54!}{60!}$.

##### Combinations (Sets)

In sets or "combinations," *repeats are not allowed* and *order doesn't matter*. For example, if ${G, Y, B}$ is in the set, then ${G, B, Y}$ and ${B, G, Y}$ cannot be in the set since order does not matter, essentially making them the same "element".

> [!info] Formula for Combinations
> $$C(n, r) = \begin{pmatrix} n \\ r \end{pmatrix} = \frac{P(n, r)}{r!} = \frac{n!}{(n - r)! r!}$$

Generally, if the elements *are* "distinguishable," then repeats are not allowed, making it a combination problem.

> [!example]
> A box of Crayola crayons has 64 unique crayons. You grab 7 of them randomly to put in your backpack.
> 
> 1. How many ways can this be done?
> 2. What is the probability that you don't grab any of these: Indigo, Cornflower, Sepia, or Periwinkle?
> 
> In this problem, we are choosing 7 items from a set of 64. Repeats are not allowed, but the order does NOT matter. Therefore, there are $\begin{pmatrix} 64 \\ 7 \end{pmatrix} = \frac{64!}{57! 7!}$ ways.
> 
> Since we are not selecting those 4 colors, then we are instead choosing 7 crayons out of a total of 60 instead of 64, so $n(E) = \begin{pmatrix} 60 \\ 7 \end{pmatrix}$. Therefore, $P(E) = \frac{\begin{pmatrix} 60 \\ 7 \end{pmatrix}}{\begin{pmatrix} 64 \\ 7 \end{pmatrix}}$.

##### Multisets (Bags)

In "multisets" (sets with repeats/bags), *repeats are allowed* and *order doesn't matter*. For example, $[R, G, G]$ is allowed since repeats are allowed. However, $[G, R, G]$ and $[G, G, R]$ are not allowed since order doesn't matter, so they are essentially the same element.

> [!info] Formula for Multisets
> $$\begin{pmatrix} n + r - 1 \\ r \end{pmatrix} = \frac{P(n + r - 1, r)}{r!} = \frac{(n + r - 1)!}{(n - 1)! r!}$$

Generally, if it says the elements are "indistinguishable," that means that repeats are allowed, making it a multiset problem.

> [!example]
> Your bag of nuts contains 10 walnuts, 8 hazelnuts, 12 pecans, and 5 almonds.
> 
> 1. How many ways are there to grab a handful of 5 nuts to feed to some squirrels?
> 2. If the nuts are selected randomly, what is the probability that the squirrels get 3 walnuts and 2 pecans?
> 
> In this problem, we are selecting 5 items from 4 different types/sets of nuts. Repeats are allowed and order does not matter, so the number of ways would be $\begin{pmatrix} 4 + 5 - 1 \\ 5 \end{pmatrix} = \begin{pmatrix} 8 \\ 5 \end{pmatrix}$.
> 
> We are choosing 3 walnuts from the set of 10 as well as 2 pecans from the set of 12, so $n(E) = \begin{pmatrix} 10 \\ 3 \end{pmatrix} \begin{pmatrix} 12 \\ 2 \end{pmatrix}$. In addition, we are choosing 5 nuts total from the set of 35, so the total sample size $n(S) = \begin{pmatrix} 35 \\ 5 \end{pmatrix}$. Therefore, the probability is $\frac{\begin{pmatrix} 10 \\ 3 \end{pmatrix} \begin{pmatrix} 12 \\ 2 \end{pmatrix}}{\begin{pmatrix} 35 \\ 5 \end{pmatrix}}$.