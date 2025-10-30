---
tags: CMSC_250
created: 2025-10-21
description: 10/15, 10/17, 10/20, 10/22, 10/29 notes (Lectures 17, 18, 19, 20, and 22)
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

Note: Make $k$ equal to what the base case was set to, and make the base case the lowest value in the domain.

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

### Constructive Induction

**Constructive** induction is an application of induction (not a type of induction) that is used to "discover" theorems and figure out the tightest bounds for a theorem.

> [!example] Constructive Induction Example
> Let $a_0 = 2$, $a_1 = 7$. For $n \geq 2$, let $a_n = 12a_{n - 1} + 3a_{n - 2}$.
> 
> We want to find the smallest positive integers $A, B$ such that: For all $n \geq 0$, $a_n \leq AB^n$.
> 
> Proof:
> I will apply strong induction on $n$.
> 
> Base case ($n =  0, 1$):
> We must satisfy these constraints:
> - $a_0 \leq AB^0$, which requires $2 \leq A$
> - $a_1 \leq AB^1$, which requires $7 \leq AB$
> 
> Inductive Hypothesis: Choose $k \geq 1$. Assume that for all $i \leq k$, $a_i \leq AB^i$.
> 
> Inductive Step: It suffices to show $a_{k + 1} \leq AB^{k + 1}$.
> 
> $a_{k + 1} = 12a_k + 3a_{k - 1}$ <---- Definition of the recurrence
> $\hspace{10mm} \leq 12AB^k + 3AB^{k - 1}$ <--- By the IH
> $\hspace{10mm} \leq AB^{k + 1}$ <--- Want to be able to derive $\leq AB^{k + 1}$
> 
> We need values of $A, B$ such that:
> $12AB^k + 3AB^{k - 1} \leq AB^{k + 1}$
> $12B + 3 \leq B^2$ <--- Dividing through by $AB^{k - 1}$
> $0 \leq B^2 - 12B - 3$
> 
> $B \geq 13$ makes the inequality true
> 
> Summary of constraints:
> - $A \geq 2$ <--- Required for base
> - $AB \geq 7$ <--- Required for base
> - $B \geq 13$ <--- Required for Inductive Step
> 
> Conclusion: For all $n \geq 0$, $a_n \leq 2(13)^n$.

### Structural Induction

> [!info] Recursive Definition
> Outline of Recursive Definition for a ***set*** of "objects":
> - Base Case(s): Describe an "atomic" object, i.e. the simplest kind of object
> - Constructor Case #1: Describe how a new object can be constructed from a collection of simpler objects
> - Constructive Case #2: Describe *another* way a new object can be constructed from a collection of simpler objects
> - Constructive Case #3: Describe *yet another* way a new object can be constructed from a collection of simpler objects
> 
> This definition must capture every possible object that we're trying to define.
> 
> This definition must not accidentally allow objects that we're NOT trying to define.

**Structural induction** works in sets of objects defined recursively.

> [!info] Structural Induction Proof
> Claim: For all $x$ in $D$: $P(x)$ \[We are assuming that $D$ is defined recursively]
> 
> Proof:
> I will apply structural induction on the set $D$.
> 
> Base case: Prove $P$ holds for any atomic object.
> 
> Inductive Hypothesis: (**NEVER STATED!**) We are about to prove that $P$ holds for an object $x$ that is a result of one of the Constructor Cases. We will assume that $P$ holds for all of the smaller elements used to construct $x$.
> 
> Inductive Step:
> Constructor 1: Show that $P$ holds for any object constructed this way.
> Constructor 2: Show that $P$ holds for any object constructed this way.