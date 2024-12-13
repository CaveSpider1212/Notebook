---
tags: MATH_220
created: 2024-10-10
description: Lesson 2.9 - Dimension and Rank
---

> [!info] Coordinates (Relative to a Basis)
> Suppose the set $B = {b_1, b_2, ..., b_p}$ is a basis for a subspace $H$. For each $x$ in $H$, the coordinates of $x$ relative to the basis $B$ are the weights $c_1, ..., c_p$ such that $x = c_1b_1 + ... + c_pb_p$, and the rector in $R^p$
> 
> $$[x]_B = \begin{bmatrix}c_1\\...\\c_p\end{bmatrix}$$
> 
> is called the coordinate vector of $x$ (relative to $B$) or the $B$-coordinate vector of $x$.

> [!info] Dimension of a Subspace
> The dimension of a nonzero subspace $H$, denoted by dim$H$, is the number of vectors in any basis for $H$. The dimension of the zero subspace ${0}$ is defined to be zero.

> [!info] Rank
> The rank of a matrix $A$, denoted by rank$A$, is the dimension of the column space of $A$.

> [!tip] The Rank Theorem
> If a matrix $A$ has $n$ columns, then rank$A +$ dim Nul$A$ = $n$.

> [!tip] The Basis Theorem
> Let $H$ be a $p$-dimensional subspace of $R^n$. Any linearly independent set of exactly $p$ elements in $H$ is automatically a basis for $H$. Also, any set of $p$ elements of $H$ that spans $H$ is automatically a basis for $H$.

> [!tip] The Invertible Matrix Theorem (adding on to [[Characterizations of Invertible Matrices#^cce62d]])
> 
> 13. The columns of $A$ form a basis of $R^n$.
> 14. Col$A$ = $R^n$
> 15. rank$A$ = $n$
> 16. dim Nul$A$ = 0
> 17. Nul$A$ = ${0}$