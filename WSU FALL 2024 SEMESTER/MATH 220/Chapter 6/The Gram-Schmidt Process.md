---
tags: MATH_220
created: 2024-11-19
description: Chapter 6.4
---

> [!tip] The Gram-Schmidt Process
> Given a basis ${x_1, ..., x_p}$ for a nonzero subspace $W$ of $R^n$, define
> 
> $v_1 = x_1$
> $v_2 = x_2 - \frac{x_2 \cdot v_1}{v_1 \cdot v_1}v_1$
> $v_3 = x_3 - \frac{x_3 \cdot v_1}{v_1 \cdot v_1}v_1 - \frac{x_3 \cdot v_2}{v_2 \cdot v_2}v_2$
> $...$
> $v_p = x_p - \frac{x_p \cdot v_1}{v_1 \cdot v_1}v_1 - \frac{x_p \cdot v_2}{v_2 \cdot v_2}v_2 - ... - \frac{x_p \cdot v_{p - 1}}{v_{p - 1} \cdot v_{p - 1}}v_{p - 1}$
> 
> Then ${v_1, ..., v_p}$ is an orthogonal basis for $W$. In addition, Span${v_1, ..., v_k}$ = Span${x_1, ..., x_k}$ for $1 \leq k \leq p$.

> [!info] Orthonormal Basis
> The orthonormal basis ([[Orthogonal Sets#^9132a9]]) of the set is found using the formula:
> 
> $$u_p = \frac{1}{||v_p||}v_p$$
> 
> This is only if the set is orthogonal. See above on finding orthogonal basis.

> [!tip] The QR Factorization
> If $A$ is an $m \times n$ matrix with linearly independent columns, then $A$ can be factored as $A = QR$, where $Q$ is an $m \times n$ matrix whose columns form an orthonormal basis for Col$A$ and $R$ is an $n \times n$ upper triangular invertible matrix with positive entries on its diagonal.