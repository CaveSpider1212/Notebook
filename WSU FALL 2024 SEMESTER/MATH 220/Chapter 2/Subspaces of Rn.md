---
tags: MATH_220
created: 2024-10-8
description: Lesson 2.8 - Subspaces of R^n
---

> [!info] Subspace (of $R^n$)
> A subspace of $R^n$ is any set $H$ in $R^n$ that has three properties:
> 
> a) The zero vector is in $H$.
> b) For each $u$ and $v$ in $H$, the sum $u + v$ is in $H$.
> c) For each $u$ in $H$ and each scalar $c$, the vector $cu$ is in $H$.
> 
> That is to say, the subspace is *closed* under addition and scalar multiplication

Two specific subspaces in the class: the column space and the null space

> [!info] Column Space
> The column space of a matrix $A$ is the set Col$A$ of all linear combinations of the columns of $A$.
> 
> If $A = \begin{bmatrix}a_1&a_2&...&a_n\end{bmatrix}$, with columns in $R^m$, then Col$A$ is the same as Span${a_1,a_2,...,a_n}$. From the first example, the column space is a subspace of $R^m$.

> [!example]
> Let $A = \begin{bmatrix}1&-3&-4\\-4&6&-2\\-3&7&6\end{bmatrix}$ and $b = \begin{bmatrix}3\\3\\-4\end{bmatrix}$. Determine whether $b$ is in the column space of $A$.
> 
> $\begin{bmatrix}1&-3&-4&|&3\\-4&6&-2&|&3\\-3&7&6&|&-4\end{bmatrix}$
> 
> (after row reducing)
> $\begin{bmatrix}1&-3&-4&|&3\\0&-6&-18&|&15\\0&0&0&|&0\end{bmatrix}$
> 
> This matrix is consistent, so $b$ is in the column space of $A$.

> [!info] Null Space
> The null space of a matrix $A$ is the set Nul$A$ of all solutions of the homogenous equation $Ax = 0$.

> [!tip] Theorem
> The null space of a $m$ x $n$ matrix $A$ is a subspace of $R^n$. Equivalently, the set of all solutions of a system $Ax = 0$ of $m$ homogenous linear equations in $n$ unknowns is a subspace of $R^n$.

Extra note about Col$A$ vs. Nul$A$:
- The null space can be described as the set of all $x$ that satisfy the equation $Ax = 0$. In a sense, it is a question concerning the domain of the transformation.
- The column space can be described as all $b$ satisfying the equation $Ax = b$. In a similar manner, we can consider this a question about the codomain of the transformation.

> [!info] Basis for a Subspace
> A basis for a subspace $H$ of $R^n$ is a linearly independent set in $H$ that spans $H$.

> [!tip] Theorem
> The pivots of a matrix $A$ form a basis for the column space of $A$.
> 
> **Warning**: You have to use the pivot columns of $A$ itself when generating the basis of Col $A$. The columns of the echelon form $B$ are not necessarily (and often not) in the column space of $A$.