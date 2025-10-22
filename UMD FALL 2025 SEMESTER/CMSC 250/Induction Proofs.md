---
tags: CMSC_250
created: 2025-10-21
description: 10/15 notes
---

Induction is another way (along with [[Proofs#^227eab | universal generalization]]) to prove universally quantified statements.

### Weak Induction

> [!info] Weak Induction Proof
> Claim: $(\forall n \in N) [P(n)]$.
> 
> Proof: I will induct on $n$.
> - Base case ($n = 0$): Show $P(0)$ directly.
> - Inductive Hypothesis: Select an arbitrary constant $k \in N$. Assume $P(k)$ is true.
> - Inductive Step: I must show $P(k + 1)$.
> - Prove $P(k + 1)$, based on the assumption that $P(k)$ is true.

### Strong Induction

> [!tip] Weak Induction vs. Strong Induction
> Weak Induction:
> - Prove the base case(s) work
> - Inductive Hypothesis: Assume proposition is true for $k$
> - Inductive Step: Show that proposition is true for $k + 1$
> 
> Strong Induction:
> - Prove the base case(s) work
> - Inductive Hypothesis: Assume proposition is true for all values from 0 through $k$
> - Inductive Step: Show that proposition is true for $k + 1$

> [!info] Strong Induction Proof
> Claim: $(\forall n \in N)[P(n)]$
> 
> Proof: I will apply strong induction on $n$.
> - Base case: Show $P(0)$, $P(1)$, $P(2)$...$P(4)$ directly.
> - Inductive Hypothesis: Let $k \geq 4$, selected arbitrarily. Assume $P(i)$ holds for all $i \leq k$.
> - Inductive Step: It suffices to show $P(k + 1)$.
> - Prove $P(k + 1)$, based on the assumption that $P$ holds for all previous values.

Note: The base case doesn't necessarily have to go to 4. However, the Inductive Hypothesis needs to have $k$ start from where the base case ended.