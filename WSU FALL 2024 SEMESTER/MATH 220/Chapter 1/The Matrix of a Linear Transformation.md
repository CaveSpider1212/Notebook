---
tags: MATH_220
created: 2024-09-17
description: Lesson 1.9 - The Matrix of a Linear Transformation
---

> [!info] Standard basis Vectors / Elementary Vectors
> A set of vectors in $R^n$ where each vector satisfies the property that exactly one of their components is one and all other components are zero.
> 
> All vectors can be written as a linear combination of elementary vectors.

> [!info] Identity Matrix
> The identity matrix is a square matrix in which all the elements of the principal diagonal are ones and all other elements are zeros.
> 
> $$\begin{bmatrix}1&0&0\\0&1&0\\0&0&1\end{bmatrix}$$

> [!tip] Theorem
> Let $T : R^n \rightarrow R^m$ be a linear transformation. Then there exists a unique matrix $A$ such that $T(x) = A(x)$ for all $x$ in $R^n$.
> 
> In fact, $A$ is the $m$ x $n$ matrix whose $j$th column is the vector $T(e_j)$, where $e_j$ is the $j$th column of the identity matrix in $R^n$.
> 
> $$A = \begin{bmatrix}T(e_1)&...&T(e_n)\end{bmatrix}$$

> [!info] Function
> A function is a relation in which every input has exactly one output.

> [!info] One-to-One Mapping
> A mapping $T : R^n \rightarrow R^m$ is one-to-one (also called injective) if each $b$ in $R^m$ is the image of at most one $x$ in $R^n$.
> 
> If there is a free variable, then there is no one-to-one mapping.

> [!info] Onto Mapping
> A mapping $T : R^n \rightarrow R^m$ is onto (also called surjective) if each $b$ in $R^m$ is the image of at least one $x$ in $R^n$.

> [!info] Bijection
> A function that is both injective and surjective (one-on-one and onto) is called a bijection.

> [!tip] Pivots in columns
> - Determine basic and free variables
> - If there's a pivot in every column, then the columns are linearly independent

> [!tip] Pivots in rows
> - Pivots in every row of a $m$ x $n$ matrix, this spans $R^m$

> [!tip] Theorem
> Let $T : R^n \rightarrow R^m$ be a linear transformation. Then $T$ is one-to-one if and only if the equation $T(x) = 0$ has only the trivial solution.

^cdf4bb

> [!tip] Theorem
> Let $T : R^n \rightarrow R^m$ be a linear transformation, and let $A$ be the standard matrix for $T$. Then:
> - $T$ maps $R^n$ onto $R^m$ if and only if the columns of $A$ span $R^m$.
> - $T$ is one-to-one if and only if the columns of $A$ are linearly independent.

^edae3b
