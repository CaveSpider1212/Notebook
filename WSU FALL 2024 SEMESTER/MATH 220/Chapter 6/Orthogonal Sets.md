---
tags: MATH_220
created: 2024-11-10
description: Chapter 6.2
---

> [!info] Orthogonal Set
> A set of vectors ${u_1, u_2, ..., u_p}$ in $R^n$ is said to be an orthogonal set if each pair of distinct vectors is orthogonal, that is, the $u_i \cdot u_j = 0$ whenever $i \neq j$.

> [!tip] Theorem
> If $S = {u_1, ..., u_p}$ is an orthogonal set of nonzero vectors in $R^n$, then $S$ is linearly independent and hence is a basis for the subspace spanned by $S$.

> [!info] Orthogonal Basis
> An orthogonal basis for a subspace $W$ of $R^n$ is a basis for $W$ is also an orthogonal set.

> [!tip] Theorem
> Let ${u_1, ..., u_p}$ be an orthogonal basis for a subspace $W$ of $R^n$. For each $y$ in $W$, the weights in the linear combination
> 
> $$y = c_1 u_1 + ... + c_p u_p$$
> 
> are given by
> 
> $$c_j = \frac{y \cdot u_j}{u_j \cdot u_j} \hspace{5mm} (j = 1, ..., p)$$

> [!info] The projection of $u$ onto $v$
> The projection of $u$ onto $v$ is given by the following equation
> 
> $$proj_v u = \frac{u \cdot v}{v \cdot v} v$$
> 
> Additionally, $proj_v u$ is occasionally described as $\hat{u}$. We can also describe the **component of** $u$ **in the direction of** $v$ by the equation
> 
> $$comp_v u = ||u|| \cos\theta = \frac{||u|| \cdot ||v|| \cos\theta}{||v||} = \frac{u \cdot v}{||v||}$$
> 
> This means that we can decompose the projection as the length of the "shadow" of $u$ projected onto $v$ times the unit vector that points in the direction of $v$.
> 
> $$proj_v u = comp_v u\left(\frac{v}{||v||}\right)= \left(\frac{u \cdot v}{||v||}\right) \left(\frac{v}{||v||}\right)= \frac{u \cdot v}{v \cdot v} v$$

> [!info] Orthonormal Basis
> A set ${u_1, ..., u_p}$ is an orthonormal set if it is an orthogonal set of unit vectors. If $W$ is the subspace spanned by such a set, then ${u_1, ..., u_p}$ is an orthonormal basis for $W$, since the set is automatically linearly independent.
> 
> Please note that the standard basis (or any nonempty subset of elementary vectors) is an orthonormal set.

^9132a9

> [!tip] Theorem
> An $m \times n$ matrix $U$ has orthonormal columns if and only if $U^T U = I$.

> [!tip] Theorem
> Let $U$ be an $m \times n$ matrix with orthonormal columns, and let $x$ and $y$ be in $R^n$. Then
> 
> 1. $||Ux|| = ||x||$
> 2. $(Ux) \cdot (Uy) = x \cdot y$
> 3. $(Ux) \cdot (Uy) = 0$ if and only if $x \cdot y = 0$

**Important Note**: The previous theorem essentially claims that linear mapping $x \rightarrow Ux$ preserves length and orthogonality.