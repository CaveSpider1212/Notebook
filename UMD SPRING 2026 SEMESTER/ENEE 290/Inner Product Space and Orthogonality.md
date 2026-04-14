---
tags: ENEE_290
created: 2026-3-2
description: 3/2, 3/9 notes (Lecture 10, 12, 13)
---

### Inner Product

> [!info] Inner Product
> Suppose that $V$ is a vector space over $F$. An **inner product** on $V$ is a function that assigns to each ordered pair of vectors $v$ and $w$ in $V$ a scalar in $F$, denoted by $\langle v, w \rangle$, such that for all $u, v, w$ in $V$ and all $r$ in $F$, we have
> 1. $\langle u + v, w \rangle = \langle u, w \rangle + \langle v, w \rangle$
> 2. $\langle rv, w \rangle = r\langle v, w \rangle$
> 3. $\bar{\langle v, w \rangle} = \langle w, v \rangle$, where the overline denotes complex conjugation (flipping the sign of the imaginary part)
> 4. $\langle v, v \rangle > 0$ if $v \neq 0$

Special case: $F = R$ and $V = R^n$

> [!info] Standard Inner Product (Dot Product)
> Let $v = (v_1, ..., v_n)$ and $w = (w_1, ..., w_n)$ be vectors in $R^n$. The **standard inner product** in $R^n$ between $v$ and $w$, denoted by $\langle v, w \rangle$, is given by
> 
> $$\langle v, w \rangle = \sum\limits_{i = 1}^{n} v_i w_i$$
> 
> This is also called the **dot product**.

Special case: $F = C$ and $V = C^n$

> [!info] Standard Inner Product
> $$\langle v, w \rangle = \sum\limits_{i = 1}^{n} v_i \bar{w}_i$$

### Norm

> [!info] Norm
> Let $V$ be an inner product space. For $v \in V$, we define the **norm** (length) of $v$ by $||v|| = \sqrt{\langle v, v \rangle}$.

If $V = R^n (n \geq 1)$, then

$$||v|| = \sqrt{\sum\limits_{i = 1}^{n} v_i^2}$$

If $V = C^n (n \geq 1)$ then

$$||v|| = \sqrt{\sum\limits_{i = 1}^{n} |v_i|^2}$$

A vector $v$ is called a **unit vector** if $||v|| = 1$.

> [!tip] Cauchy-Schwartz Inequality
> Suppose that $V$ is an inner product space and $u, v \in V$. Then,
> 
> $$|\langle u, v \rangle|^2 \leq  \langle u, u \rangle \cdot \langle v, v \rangle = ||u||^2 \cdot ||v||^2$$

> [!tip] Theorem
> Let $V$ be an inner product space over $F$. Then, for all $u, v \in V$ and $r \in F$, the following hold:
> 1. $||ru|| = |r| \cdot ||u||$
> 2. $||v|| = 0$ if and only if $v = 0$
> 3. $|\langle u, v \rangle| \leq ||u|| \cdot ||v||$
> 4. $||u + v|| \leq ||u|| + ||v||$ (triangle inequality)

### Orthogonal Vectors and Sets

> [!info] Orthogonal
> Two vectors $u$ and $v$ in an inner product space $V$ are said to be **orthogonal** if $\langle u, v \rangle = 0$.

> [!info] Orthogonal Set
> A set of nonzero vectors $\{ v_1, v_2, ..., v_m \}$ in an inner product space $V$ is called an **orthogonal set** of vectors if
> 
> $$\langle v_i, v_j \rangle = 0$$
> 
> for all $i \neq j$.

^04e6f7

### Orthonormal Sets

> [!info] Orthonormal Set
> An orthogonal set of *unit vectors* is called an **orthonormal set** of vectors (i.e. $\{ v_1, v_2, ..., v_m \}$ is orthonormal) if and only if
> 1. $\langle v_i, v_j \rangle = 0$ for all $i \neq j$
> 2. $\langle v_i, v_i \rangle = ||v_i||^2 = 1$ for all $i = 1, ..., m$

> [!info] Unit Vectors
> Suppose that $v$ is a nonzero vector in an inner product space $V$. Then, we can construct a unit vector
> 
> $$u = \frac{1}{||v||}v$$
> 
> where $||u|| = 1$.

> [!info] Normalization
> Given an orthogonal set $\{ v_1, v_2, ..., v_m \}$, we can construct an orthonormal set $\{ u_1, u_2, ..., u_m \}$ where $u_i = \frac{v_i}{||v_i||}$. This process is called **normalization**.

### Orthogonal/Orthonormal Bases

> [!info] Orthogonal and Orthonormal Bases
> A basis $B = \{ v_1, v_2, ..., v_m \}$ for a (finite-dimensional) inner product space is called an **orthogonal basis** if the basis $B$ is an [[Inner Product Space and Orthogonality#^04e6f7|orthogonal set]].
> 
> Moreover, if the basis is orthonormal, i.e., $||v_i|| = 1$ for all $i = 1, ..., m$, it is called an **orthonormal basis**.

> [!tip] Theorem
> Suppose $\{ v_1, v_2, ..., v_m \}$ is an *orthogonal set* of nonzero vectors in an inner product space. Then, $\{ v_1, v_2, ..., v_m \}$ is *linearly independent*.

If $B = \{ v_1, v_2, ..., v_m \}$ is an orthogonal basis for inner product space $V$, then any vector $u \in V$ can be written *uniquely* as

$$u = c_1 v_1 + ... + c_n v_n$$ 

$$c_i = \frac{\langle u, v_i \rangle}{||v_i||^2}$$

If $B = \{ v_1, v_2, ..., v_m \}$ is an *orthonormal* basis, then the length/norm is equal to 1, so:

$$u = \langle u, v_1 \rangle v_1 + ... + \langle u, v_n \rangle v_n$$

### Gram-Schmidt Process

If $B$ is a basis that is not necessarily orthogonal, we can find an orthogonal basis from $B$ using the Gram-Schmidt Process.

> [!info] Gram-Schmidt Process
> $$u_n = v_n - \sum\limits_{k = 1}^{n - 1} \frac{\langle v_n, u_k \rangle}{||u_k||^2} u_k$$

### Projection

> [!info] Projection
> Suppose that $W \subseteq V$ is a subspace of an inner product space $V$ and that $V \in V \backslash W$. Then, the vector $v$ can be *uniquely* written as a sum $v_W + v_{\perp}$, where $v_W \in W$ and $\langle w, v_{\perp} \rangle = 0$ for all $w \in W$.
> 
> $v_W$ is called the **projection** of $v$ onto $W$, $v_W = \text{proj}_W (v)$.

Suppose $\{ w_1, w_2, ..., w_k \}$ is an *orthogonal* basis for $W$. Then,

$$v_W = \frac{\langle v, w_1 \rangle}{||w_1||^2} w_1 + ... + \frac{\langle v, w_k \rangle}{||w_k||^2} w_k$$