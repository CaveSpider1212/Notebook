---
tags: MATH_220
created: 2024-11-14
description: Chapter 6.3
---

Goal for this section: We want to show that given a vector $y$ and a subspace $W$ there **exists** a vector $\hat{y}$ in $W$ such that

1. $\hat{y}$ is the **unique** vector in $W$ for which $y - \hat{y}$ is orthogonal to $W$
2. $\hat{y}$ is the **unique** vector in $W$ "closest" to $y$.

Note: We don't actually need an orthogonal basis for $R^n$. It is sufficient to have an orthogonal basis for $W$.

> [!tip] Theorem: The Orthogonal Decomposition Theorem
> Let $W$ be a subspace of $R^n$. Then each $y$ in $R^n$ can be written uniquely in the form
> 
> $$y = \hat{y} + z$$
> 
> where $\hat{y}$ is in $W$ and $z$ is in $W^{\perp}$. In fact, if ${u_1, ..., u_p}$ is any orthogonal basis of $W$, then
> 
> $$\hat{y} = \frac{y \cdot u_1}{u_1 \cdot u_1}u_1 + ... + \frac{y \cdot u_p}{u_p \cdot u_p}u_p$$
> 
> and $z = y - \hat{y}$

Note: The vector $\hat{y}$ is called the orthogonal projection of $y$ onto $W$ and is often expressed as proj$_Wy$.

> [!tip] The Best Approximation Theorem
> Let $W$ be a subspace of $R^n$, let $y$ be any vector in $R^n$, and let $\hat{y}$ be the orthogonal projection of $y$ onto $W$. Then $\hat{y}$ is the closest point in $W$ to $y$, in the sense that
> 
> $$||y - \hat{y}|| < ||y - v||$$
> 
> for all $v$ in $W$ distinct from $\hat{y}$.

> [!tip] Theorem
> If ${u_1, ..., u_p}$ is an orthonormal basis for a subspace $W$ of $R^n$, then
> 
> $$proj_W y = (y \cdot u_1)u_1 + (y \cdot u_2)u_2 + ... + (y \cdot u_p)u_p$$
> 
> If $U = \begin{bmatrix}u_1&&u_2&&...&&u_p\end{bmatrix}$, then
> 
> $$proj_W y = U U^T y$$
> 
> for all $y$ in $R^n$

Given that $U$ is an $n \times p$ matrix with orthonormal columns, and $W$ is the column space of $U$, then
- $U^T Ux = I_p x = x$ for all $x$ in $R^p$
	- By Theorem from previous class, [[Inner Product, Length, and Orthogonality]]
- $U U^T y = proj_W y$ for all $y$ in $R^n$
	- By previous theorem

If $U$ is a square matrix with orthonormal columns, then $U$ is an *orthogonal* matrix. The column space $W$ is all of $R^n$, and $U U^T y = Iy = y$ for all $y$ in $R^n$.

