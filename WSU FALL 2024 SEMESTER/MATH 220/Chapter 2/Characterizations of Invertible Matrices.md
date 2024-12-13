---
tags: MATH_220
created: 2024-10-3
description: Lesson 2.3 - Characterizations of Invertible Matrices
---

> [!tip] The Invertible Matrix Theorem
> Let $A$ be a square $n$ x $n$ matrix. Then the following statements are equivalent, meaning they're either all true or all false for $A$.
> 
> 1. $A$ is an invertible matrix.
> 2. $A$ is row equivalent to the $n$ x $n$ identity matrix.
> 3. $A$ has $n$ pivot positions.
> 4. The equation $Ax = 0$ has only the trivial solution.
> 5. The columns of $A$ form a linearly independent set.
> 6. The linear transformation $x \rightarrow Ax$ is one-to-one.
> 7. The equation $Ax = b$ has at least one solution for each $b$ in $R^n$
> 8. The columns of $A$ span $R^n$.
> 9. The linear transformations $x \rightarrow Ax$ maps $R^n$ onto $R^n$.
> 10. There is an $n$ x $n$ matrix $C$ such that $CA = I$.
> 11. There is an $n$ x $n$ matrix $D$ such that $AD = I$.
> 12. $A^T$ is an invertible matrix.

^cce62d

Each statement in this theorem can be proved, and so can the [[The Matrix Equation Ax = b#^859146]], [[The Matrix of a Linear Transformation#^edae3b]], and [[The Matrix of a Linear Transformation#^cdf4bb]] theorems in older chapters.

> [!tip] Theorem
> Let $T : R^n \rightarrow R^n$ be a linear transformation and let $A$ be the standard matrix for $T$. Then $T$ is invertible if and only if $A$ is an invertible matrix. In that case, the linear transformations $S(x) = A^{-1}x$ is the unique function satisfying the following
> 
> 1. $S(T(x)) = x$ for all $x$ in $R^n$
> 2. $T(S(x)) = x$ for all $x$ in $R^n$