---
tags: ENEE_290
created: 2026-3-9
description: 3/11, 3/23 notes (Lecture 13, 14)
---

### Matrices

> [!info] Matrix
> An $m \times n$ matrix is a rectangular 2D array of numbers arranged in $m$ rows and $n$ columns. The entries in a matrix are called the **elements** of the matrix.
> 
> $$A = \begin{bmatrix} a_{1, 1} & a_{1, 2} & ... & a_{1, n} \\ a_{2, 1} & a_{2, 2} & ... & a_{2, n} \\ ... & ... & ... & ... \\ a_{m, 1} & a_{m, 2} & ... & a_{m, n} \end{bmatrix}$$

Two matrices $A$ and $B$ are *equal*, written $A = B$, if and only if they have the same size and all corresponding elements are equal.

### Matrix Addition

Addition is done with matrices of the same dimension, and the corresponding elements in each position of the matrix are added together.

### Scalar Multiplication

Scalar multiplication with matrices is done by multiplying each element in the matrix by the scalar.

### Transpose of a Matrix

Suppose $A$ is an $m \times n$ matrix. Then, its **transpose** ($A^T$) is an $n \times m$ matrix such that the i-th row of $A^T$ contains the elements of the i-th column of $A$.

### Square Matrices

> [!info] Square Matrix
> An $n \times n$ matrix $A$ is called a **square matrix**, meaning it hash the same number of rows as the number of columns.
> 
> The **diagonal elements** are the elements in the main/leading diagonal ($a_{1, 1}, 1 \leq i \leq n$).
> 
> A square matrix satisfying $a_{i, j = 0}$ for all $i < j$ is said to be **lower triangular** (upper triangular for all $i > j$).
> 
> A square matrix is said to be **diagonal** if $a_{i, j} = 0$ for all $i \neq j$ (meaning it is both upper and lower triangular).

### Symmetric Matrices

A $n \times n$ square matrix $A$ is said to be **symmetric** if $A = A^T$.

### Matrix Multiplication

> [!info] Matrix Multiplication
> Suppose $A \in R^{m \times n}$ and $C \in R^{n \times p}$.
> 
> Elements in the i-th row and j-th column of $AC$ is given by the (dot) product of the i-th row of $A$ and the j-th column of $C$.
> 
> It requires that the number of columns of $A$ is equal to the number of rows in $C$.
> 
> $AC \in R^{m \times p}$, meaning it has $m$ rows and $p$ columns.

Each column of $AC$ would be a different linear combination of the columns of $A$.

> [!example] Matrix Multiplication Example
> $\begin{bmatrix} 3&1&2\\5&4&7 \end{bmatrix} \times \begin{bmatrix} 4&2\\3&5\\1&4 \end{bmatrix}$ = ?
> 
> $\begin{bmatrix} (3 \times 4) + (1 \times 3) + (2 \times 1) & (3 \times 2) + (1 \times 5) + (2 \times 4) \\ (5 \times 4) + (4 \times 3) + (7 \times 1) & (5 \times 2) + (4 \times 5) + (7 \times 4) \end{bmatrix}$
> $= \begin{bmatrix} 17&19\\39&58 \end{bmatrix}$



### Properties of Matrix Operations

> [!tip] Theorem
> Suppose $A, B, C$ are matrices of appropriate dimensions. THe matrix multiplication satisfies the following properties:
> - Associativity
> - Left distributivity
> - Right distributivity

Matrix multiplication is *not* commutative, even when the two matrices are both square matrices.