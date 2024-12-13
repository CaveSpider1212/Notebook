---
tags: MATH_220
created: 2024-10-01
description: Lesson 2.2 - Inverses
---

> [!info] Invertible
> A square matrix $A$ is invertible if there exists a matrix $B$ such that $AB = I$ and $BA = I$. The inverse of $A$ is typically denoted $A^{-1}$.
> 
> Basically, multiply them, and the should equal $\begin{bmatrix}1&0&0\\0&1&0\\0&0&1\end{bmatrix}$.

> [!info] Elementary Matrices
> An elementary matrix is a matrix that describes an elementary row operation on an identity matrix.

> [!info] Finding $A^{-1}$
> To find $A^{-1}$ we will row reduce the augmented matrix $\begin{bmatrix}A&&I\end{bmatrix}$. The result will either give $\begin{bmatrix}I&&A^{-1}\end{bmatrix}$, or it will be impossible to row reduce $A$ to the identity. If $A$ cannot be reduced to $I$, then $A$ does not have an inverse.
> 
> Basically, if $I$ in the second matrix ends up having a 0 row, then $A$ doesn't have an inverse.
> 
> If $A$ is an invertible $n$ x $n$ matrix, then we know $Ax = b$ has at least one solution ($x = A^{-1}b$)

> [!example]
> Find the inverse of $A$ given that $A = \begin{bmatrix}0&1&2\\1&0&3\\4&-3&8\end{bmatrix}$.
> 
> $\begin{bmatrix}0&1&2&|&1&0&0\\1&0&3&|&0&1&0\\4&-3&8&|&0&0&1\end{bmatrix}$
> 
> (after using multiple row operations)
> $\begin{bmatrix}1&0&0&|&\frac{-9}{2}&7&\frac{-3}{2}\\0&1&0&|&-2&4&-1\\0&0&1&|&\frac{3}{2}&-2&\frac{1}{2}\end{bmatrix}$

> [!tip] Theorem
> 1. If $A$ is an invertible matrix, then $A^{-1}$ is invertible and
> $$(A^{-1})^{-1} = A$$
> 2. If $A$ and $B$ are $n$ x $n$ invertible matrices, then so is $AB$, and the inverse of $AB$ is the product of the inverses of $A$ and $B$ in reverse order. That is,
> $$(AB)^{-1} = B^{-1}A^{-1}$$
> 3. If $A$ is an invertible matrix, then so is $A^T$, and the inverse of $A^T$ is the transpose of $A^{-1}$. That is,
> $$(A^T)^{-1} = (A^{-1})^T$$
> 4. An $n$ x $n$ matrix $A$ is invertible if and only if $A$ is row equivalent to $I_n$.