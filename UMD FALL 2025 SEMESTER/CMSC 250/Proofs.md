---
tags: CMSC_250
created: 2025-9-22
description: 9/19, 9/22 notes
---

### Writing Proofs

A good proof should have:
- "Claim:" -- a statement of what is to be proven
- "Proof:" -- indication of where the proof starts
- Step by step derivation starting with premises/assumptions and ending with the desired conclusion
- Each step must logically follow the step above
- There should be a clear justification for each step

### Rules of Inference with Quantifiers

> [!info] Existential Generalization
> $P(a)$ for some $a \in D$
> $\therefore (\exists x \in D)[P(x)]$

> [!info] Universal Instantiation
> $(\forall x \in D)[P(x)]$
> $\therefore P(a)$ for any particular $a \in D$

> [!info] Existential Instantiation
> $(\exists x \in D)[P(x)]$
> $\therefore P(a)$ for *some* $a \in D$

> [!info] Universal Generalization
> Let $a \in D$ (selected arbitrarily)
> 
> $P(a)$
> $\therefore (\forall x \in D)[P(x)]$

### Constructive Proofs of Existence

Constructive proofs of existence are essentially providing a method or algorithm to demonstrate that some mathematical thing exists through an explicit example or formula.

> [!example]
> **Claim**: There exist three *distinct* natural numbers $a$, $b$, and $c$ such that $a^2 + b^2 = c^2$.
> 
> **Proof**:
> Let $a = 3$, $b = 4$, and $c = 5$.
> $a$, $b$, and $c$ are distinct, and $a^2 + b^2 = 3^2 + 4^2 = 25 = 5^2 = c^2$, as desired.

> [!example]
> **Claim**: $2^{66} - 1$ is composite.
> 
> **Proof**:
> $2^{66} - 1$ is composite.
> Since each of these factors is greater than 1 (and less than $2^{66} - 1$), each is a "non-trivial" factor, hence $2^{66} - 1$ is composite, as desired.

### Proofs by Exhaustion (Cases)

Proof by exhaustion is essentially using "brute force" to try and prove a claim, substituting in cases or numbers into the statement to test it.

> [!example]
> **Claim**: There are no integer solutions to the equation $a^2 + b^2 = 7$.
> 
> **Proof**:
> Since squares must be non-negative, neither term ($a^2$ or $b^2$) can exceed 7. The only squares that are less than or equal to 7 are 0, 1, and 4, so we need only consider those values for each term.
> 
> Case "*Both terms are 0*": $0 + 0 \neq 7$, so that doesn't work.
> Case "*Both terms are 1*": $1 + 1 \neq 7$, so that doesn't work.
> Case "*Both terms are 4*": $4 + 4 \neq 7$, so that doesn't work.
> Case "*One term is 0 and the other is 1*": $0 + 1 \neq 7$, so that doesn't work.
> Case "*One term is 0 and the other is 4*": $0 + 4 \neq 7$, so that doesn't work.
> Case "*One term is 1 and the other is 4*": $1 + 4 \neq 7$, so that doesn't work.
> 
> These cases exhaust all possibilities, and in no case is there an integer solution to $a^2 + b^2 = 7$.

> [!example]
> **Claim**: 23 cannot be written as the sum of 8 non-negative cubes.
> 
> **Proof**:
> We need only consider cubes that are less than 23, so we may restrict our attention to terms equal to 0, 1, or 8.  Note that there can be at most 2 terms equal to 8, without exceeding 23, so we’ll divide into cases based on how many terms are equal to 8.
> 
> Case "*There are no 8's*": All terms are less than or equal to one, so their sum could be no more than 8, far short of 23.
> Case "*There is exactly one 8*": We need the other seven terms to sum to 15. But that's impossible. All other terms are less than or equal to one, so their sum could only reach 7, far short of 15.
> Case "*There are exactly two 8's*": We need the other six terms to sum to 7. Again that's impossible. The other six terms are less than or equal to one, so their sum could only reach 6, which is short of reaching 7.
> 
> These cases are exhaustive and in no case is it possible to obtain 8 non-negative cubes that sum to 23.