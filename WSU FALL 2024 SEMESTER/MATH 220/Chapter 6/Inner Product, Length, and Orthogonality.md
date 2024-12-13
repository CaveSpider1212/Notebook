---
tags: MATH_220
created: 2024-11-12
description: Chapter 6.1
---

> [!info] Inner Product (Dot Product)
> Given two vectors, $u$ and $v$, in $R^n$, the number $u^T v$ is called the inner product of $u$ and $v$ and is typically written as $u \cdot v$.
> 
> $$u \cdot v = u^T v$$

> [!tip] Theorem: Dot Product Properties
> Let $u$, $v$ and $w$ be vectors in $R^n$ and let $c$ be a scalar.
> 
> 1. $u \cdot v = v \cdot u$
> 2. $(u + v) \cdot w = u \cdot w + v \cdot w$
> 3. $(cu) \cdot v = c(u \cdot v) = u \cdot (cv)$
> 4. $u \cdot v \ge 0$, and $u \cdot u = 0$ if and only if $u = 0$.

> [!info] Vector Length (Norm)
> The length (or norm) of a vector $v$ is the nonnegative scalar $||v||$ defined by
> 
> $$||v|| = \sqrt{v \cdot v} = \sqrt{v_1^2 + v_2^2 + ... + v_n^2}$$
> $$||v||^2 = v \cdot v$$

> [!info] Unit Vector
> A vector whose length is 1 is called a unit vector.

> [!info] Distance Between $u$ and $v$
> For $u$ and $v$ in $R^n$, the distance between $u$ and $v$, written as dist$(u, v)$, is the length of the vector $u - v$. That is,
> 
> $$dist(u - v) = ||u - v||$$

> [!info] Orthogonal Vectors
> Two vectors $u$ and $v$ in $R^n$ are orthogonal (to each other) if $u \cdot v = 0$

> [!tip] The Pythagorean Theorem
> Two vectors $u$ and $v$ are orthogonal if and only if $||u + v||^2 = ||u||^2 + ||v||^2$.

> [!info] Orthogonal Complement
> If a vector $z$ is orthogonal to every vector in a subspace $W$ of $R^n$, then $z$ is said to be orthogonal to $W$.
> 
> The set of all vectors $z$ that are orthogonal to $W$ is called the orthogonal complement of $W$ and is denoted by $W^{\perp}$ (read as $W$ perpendicular or $W$ perp).

Additional Notes:
- A vector $x$ is in $W^{\perp}$ if and only if $x$ is orthogonal to every vector in a set that spans $W$.
- $W^{\perp}$ is a subspace of $R^n$

> [!info] Row Space
> The row space of $A$ is defined to be the column space of $A^T$. That is to say, the row space of $A$ is the span of its row vectors.

> [!tip] Theorem
> Let $A$ be an $m \times n$ matrix. The orthogonal complement of the row space of $A$ is the null space of $A$, and the orthogonal complement of the column space of $A$ is the null space of $A^T$.

> [!info] Dot Product (Alternative Definition)
> 
> $$u \cdot v = ||u|| ||v|| \cos\theta$$
> 
> Note: we generally use the component-wise definition for calculating the dot product. The definition above is usually reserved to find the angle between the vectors.
> 
> $$\cos\theta = \frac{u \cdot v}{||u|| ||v||}$$