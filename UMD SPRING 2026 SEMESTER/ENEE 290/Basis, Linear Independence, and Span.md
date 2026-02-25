---
tags: ENEE_290
created: 2026-2-23
description: 2/23 notes (Lecture 8)
---

### Linear Independence

> [!info] Linear Independence
> A finite nonempty set of vectors $\{ v_1, v_2, ..., v_m \} \subset V$ is said to be **linearly dependent** if there exists scalars $c_1, ..., c_m$ not all of which are equal to zero, such that
> 
> $$c_1 v_1 + c_2 v_2 + ... + c_m v_m = 0$$
> 
> Similarly, a finite nonempty set of vectors $\{ v_1, v_2, ..., v_m \} \subset V$ is said to be **linearly independent** if only $c_1 = c_2 = ... = c_m = 0$ satisfy the equality above.

### Spanning Set

> [!info] Spanning Set
> Considering a set of vectors $\{ v_1, v_2, ..., v_m \}$. If every vector in a vector space $V$ can be written as a linear combination of the vectors in the set, we say that $V$ is *spanned* or *generated* by the set, and call the set $\{ v_1, v_2, ..., v_m \}$ a **spanning set** for $V$. Also, we say that $\{ v_1, v_2, ..., v_m \}$ *spans* $V$.

### Linear Span

> [!info] Linear Span
> Consider a set of vectors $\{ v_1, v_2, ..., v_m \}$ in a vector space $V$. Let
> 
> $$S = \{ \sum\limits_{i = 1}^{m} c_i v_i | c_1, ..., c_m \in F \}$$
> 
> be the set of all vectors in $V$ which can be written as linear combinations of $v_1, v_2, ..., v_m$. We call $S$ the **linear span** of the set $\{ v_1, v_2, ... v_m \}$ and denote it by $\text{span} \{ v_1, v_2, ..., v_m \}$.

> [!tip] Theorem
> Let $v_1, v_2, ..., v_m$ be vectors in a vector space $V$. Then, the linear span
> 
> $$S = \text{span} \{ v_1, v_2, ..., v_m \} = \{ \sum\limits_{i = 1}^{m} c_i v_i | c_1, ..., c_m \in F \}$$
> 
> is a subspace of $V$

### Basis

> [!info] Basis
> A **basis** for a vector space $V$ is a set of vectors
> 
> $$B = \{ b_1, b_2, ..., b_m \}$$
> 
> in $V$, which is *linearly independent* and *spans the vector space $V$*