---
tags: MATH_220
created: 2024-12-3
description: Chapter 6.5
---

> [!info] Least-Squares Solutions
> If $A$ is $m \times n$ and $b$ is in $R^m$, a least-squares solution of $Ax = b$ is an $\hat{x}$ in $R^n$ such that
> 
> $$||b - A\hat{x}|| \leq ||b - Ax||$$
> 
> for all $x$ in $R^n$.

> [!tip] Theorem
> The set of least-squares solutions of $Ax = b$ coincides with the nonempty set of solutions of the normal equations $A^T Ax = A^T b$.

> [!tip] Theorem
> Let $A$ be an $m \times n$ matrix. The following statements are logically equivalent:
> 
> a) The equation $Ax = b$ has a unique least-squares solution for each $b$ in $R^m$.
> b) The columns of $A$ are linearly independent.
> c) The matrix $A^T A$ is invertible.
> 
> When these statements are true, the least-squares solution $\hat{x}$ is given by
> 
> $$\hat{x} = (A^T A)^{-1} A^T b$$

Extra Note: When a least-squares solution $\hat{x}$ is used to produce $A\hat{x}$ as an approximation to $b$, the distance from $b$ to $A\hat{x}$ is called the least-squares error of this approximation.

> [!tip] Theorem
> Given an $m \times n$ matrix $A$ with linearly independent columns, let $A = QR$ be a $QR$ factorization of $A$. Then, for each $b$ in $R^m$, the equations $Ax = b$ has a unique least-squares solution, given by
> 
> $$\hat{x} = R^{-1} Q^T b$$