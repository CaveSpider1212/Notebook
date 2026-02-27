---
tags: ENEE_290
created: 2026-2-23
description: 2/23, 2/25 notes (Lecture 8, 9)
---

### Linear Independence

> [!info] Linear Independence
> A finite nonempty set of vectors $\{ v_1, v_2, ..., v_m \} \subset V$ is said to be **linearly dependent** if there exists scalars $c_1, ..., c_m$ not all of which are equal to zero, such that
> 
> $$c_1 v_1 + c_2 v_2 + ... + c_m v_m = 0$$
> 
> Similarly, a finite nonempty set of vectors $\{ v_1, v_2, ..., v_m \} \subset V$ is said to be **linearly independent** if only $c_1 = c_2 = ... = c_m = 0$ satisfy the equality above.

If at least one of the vectors in the set can be written as a linear combination of the other vectors in the set, then the set is linearly dependent.

### Spanning Set

> [!info] Spanning Set
> Considering a set of vectors $\{ v_1, v_2, ..., v_m \}$. If every vector in a vector space $V$ can be written as a linear combination of the vectors in the set, we say that $V$ is *spanned* or *generated* by the set, and call the set $\{ v_1, v_2, ..., v_m \}$ a **spanning set** for $V$. Also, we say that $\{ v_1, v_2, ..., v_m \}$ *spans* $V$.
> 
> If it is a $n$-dimensional space but the set does not have $n$ vectors in it, then it does not span the vector space.

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
> in $V$, which is *linearly independent* and *spans the vector space $V$*.

$B$ spans $V$ if and only if any vector $v \in V$ can be written as a linear combination of the vectors in $B$

$$v = c_1 b_1 + c_2 b_2 + ... + c_m b_m$$

for some scalars $c_1, c_2, ..., c_m$.

> [!tip] Theorem
> Suppose that a vector space $V$ has a *finite* basis
> 
> $$B = \{ v_1, v_2, ..., v_m \}$$
> 
> Then, all bases for $V$ have the same number of vectors.

There is a unique representation of each vector as a linear combination of $m$ vectors in the basis.

### Dimension of a Vector Space

> [!info] Dimension
> The **dimension** of a vector space (with a finite basis) is the number of vectors in a basis (denoted by $\text{dim} (V)$).

1. A vector space with a finite basis is said to be *finite dimensional*
2. Since all bases have the same number of vectors, there is no issue with the above definition of its dimension
3. The number of vectors in a linearly independent set in a finite dimensional vector space cannot exceed the dimension of the vector space.

Dimension is the "size" of the space in terms of coordinates. 

> [!tip] Theorem
> If $\text{dim} (V) = n$, *any* set of $n$ linearly independent vectors in $V$ is a basis for $V$

Suppose that $V$ is a vector space of dimension $n$ and $S = \{ v_1, v_2, ..., v_n \}$ is a subset of $n$ vectors in $V$. Then, the following statements are equivalent:
1. $S$ is a basis for $V$
2. $S$ is linearly independent
3. $S$ spans $V$

> [!tip] Theorem
> Suppose that $S$ is a subspace of a vector space $V$ of dimension $n$. Then, $\text{dim}(S) \leq \text{dim}(V)$. Moreover, if $\text{dim}(V) = \text{dim}(S)$, then $S = V$

### Inner Product

> [!info] Inner Product
> Suppose that $V$ is a vector space over $F$. An **inner product** on $V$ is a function that assigns to each ordered pair of vectors $v$ and $w$ in $V$ a scalar in $F$, denoted by $\langle v, w \rangle$, such that for all $u, v, w$ in $V$ and all $r$ in $F$, we have
> 1. $\langle u + v, w \rangle = \langle u, w \rangle + \langle v, w \rangle$
> 2. $\langle rv, w \rangle = r\langle v, w \rangle$
> 3. $\bar{\langle v, w \rangle} = \langle w, v \rangle$, where the overline denotes complex conjugation
> 4. $\langle v, v \rangle > 0$ if $v \neq 0$