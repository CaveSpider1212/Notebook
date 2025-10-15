---
tags: CMSC_250
created: 2025-9-22
description: 9/19, 9/22 notes
---

### Closure

> [!info]
> A binary operation on a set is closed if, for any two elements chosen in the set, the result of the operation on those two elements is also within the same set.

![[9.17.25 Closure Table.png]]

### Writing Proofs

A good proof should have:
- "Claim:" -- a statement of what is to be proven
- "Proof:" -- indication of where the proof starts
- Step by step derivation starting with premises/assumptions and ending with the desired conclusion
- Each step must logically follow the step above
- There should be a clear justification for each step

##### Important notes relating to proofs

$a \vert b$: "$a$ divides $b$" or "$a$ is a factor of $b$" or "$b$ is a multiple of $a$"
$a \vert b$ if and only if $b = ak$ for some $k \in Z$ or $N$ (depending on the domain)

If $a$ is even, then it can be expressed as $a = 2k$ for some $k \in Z$.
If $a$ is odd, then it can be expressed as $a = 2k + 1$ for some $k \in Z$.

If $a$ is composite, then it has "non-trivial" factors (factors other than 1 and itself), and if $A$ is a polynomial, we can see if it is composite if it can be factored.

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
> 
> Note: When proving these, it is important to say something like "Let $a \in D$, selected arbitrarily" followed by proving how $a$ makes the statement true and concluding it, ending with something like "Since $a$ was selected arbitrarily, the proposition holds for any element in $D$"

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
> $2^{66} - 1 = (2^{33} - 1)(2^{33} + 1)$.
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

The last sentence ("These cases exhaust all possibilities...") is important for proofs by exhaustion.

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

### Proving Implications

"If $P$ then $Q$"

> [!info]  Proving Implications
> Claim: If $P$ then $Q$
> 
> Proof: Assume $P$
> ...
> $Q$

> [!info] Proving Implications (Universal Generalization)
> Claim: $(\forall x \in D)$ \[If $P(x)$ then $Q(x)$]
> 
> Proof: Let $a \in D$, selected arbitrarily.
> Assume $P(x)$ holds. \[I will show $Q(x)$]
> ...
> $Q(a)$
> $\therefore P(a) \rightarrow Q(a)$.
> Since $a$ was selected arbitrarily, the proposition holds for any element in $D$.

### Proof by Contrapositive

Since $P \rightarrow Q \equiv \sim Q \rightarrow \sim P$, assume $\sim Q$ first.

> [!info] Proof by Contrapositive
> Claim: If $P$ then $Q$.
> Proof: I will prove by contraposition.
> Assume $\sim Q$.
> ...
> $\sim P$

### Proofs of Biconditional Statements

To prove $P \leftrightarrow Q$, a [[Conditionals and Biconditional Statements#^8139f1|biconditional statement]], show that $P \rightarrow Q$ is true in one part, then show $Q \rightarrow P$ in another part.

### Proofs by Contradiction

To prove $P$ is true, prove that $\sim P$ will lead to a contradiction.

> [!info] Proofs by Contradiction
> Claim: $P$
> 
> Proof: Suppose (BWOC, by way of contradiction) $\sim P$.
> ...
> Contradiction

### Fundamental Theorem of Arithmetic

> [!tip] Fundamental Theorem of Arithmetic
> For any $n > 1$:
> - $n$ can be expressed as the product of primes ("existence")
> - The prime factorization of $n$ is unique ("uniqueness")

In proofs, can be written as:
- $n = 2^{e1} \times 3^{e2} \times 5^{e3} \times ... \times p_k^{ek}$ (the exponents can be 0)
- $n = p_1^{e1} \times p_2^{e2} \times p_3^{e3} \times ... \times p_k^{ek}$

##### "Uniqueness"

If $a = b$ then $a$ and $b$ share the same prime factorization.

### Modular Congruence

> [!info] Modulo Operations
> "$a$ mod $n$" represents the remainder when $a$ is divided by $n$.
> 
> The result is always between $0$ and $n - 1$.

$a \equiv_{n} b$: $a$ mod $n$ $=$ $b$ mod $n$

> [!tip] Congruence Theorem
> For all $a, b \in N$, the following are equivalent:
> 1. $a \equiv_{n} b$
> 2. $n \vert (a - b)$
> 3. $(\exists k \in Z)[a = b + kn]$

### Modular Arithmetic Theorem (MAT)

> [!tip] Modular Arithmetic Theorem (MAT)
> Let $a, b, c, d, n \in Z$, and $n > 1$. Suppose $a \equiv_{n} c$ and $b \equiv_{n} d$. Then:
> 1. $(a + b) \equiv_{n} (c + d)$
> 2. $(a - b) \equiv_{n} (c - d)$
> 3. $ab \equiv_{n} cd$
> 4. $a^m \equiv_{n} c^m$ for all $m \geq 1$

### Quotient-Remainder Theorem

> [!tip] Quotient-Remainder Theorem
> $$(\forall a \in Z)(\forall n \in Z^+)(\exists q, r \in Z)[(a = qn + r) \land (0 \leq r \leq n)]$$
> 
> "We can find $q$ so that $r$ comes out between $0$ and $n - 1$."

### Proofs with Floor and Ceiling

> [!info] Floor
> $\lfloor x \rfloor$: Floor of $x$ (rounded down)
> 
> Definition: For all $x \in R$, $\lfloor x \rfloor$ is the unique integer such that $\lfloor x \rfloor \leq x \lt \lfloor x \rfloor + 1$.

> [!info] Ceiling
> $\lceil x \rceil$: Ceiling of $x$ (rounded up)
> 
> Definition: For all $x \in R$, $\lceil x \rceil$ is the unique integer such that $\lceil x \rceil - 1 \lt x \leq \lceil x \rceil$.