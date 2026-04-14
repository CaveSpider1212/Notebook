---
tags: ENEE_290
created: 2026-4-1
description: 4/1, 4/6, 4/8 notes (Lecture 17, 18, 19)
---

### Transformation

> [!info] Transformation
> A **transformation** from $\mathbb{R}^n$ to $\mathbb{R}^m$ is mapping $T$ that assigns to each vector $v \in \mathbb{R}^n$ another vector $T(v) \in \mathbb{R}^m$.
> 
> $$T : \mathbb{R}^n \rightarrow \mathbb{R}^m$$
> 
> $\mathbb{R}^n$: domain of $T$
> $\mathbb{R}^m$: codomain of $T$
> $T(v)$:: image of $v \in \mathbb{R}^n$
> $\{ T(v) | v \in \mathbb{R}^n \} \subseteq \mathbb{R}^m$: image of $T$

### Matrix and Linear Transformation

> [!info] Matrix Transformation
> The **matrix transformation** associated with matrix $A$ is the transformation $T : \mathbb{R}^n \rightarrow \mathbb{R}^m$ defined by $T(v) = Av \in \mathbb{R}^m$.
> 
> $$T_A (v)$$

> [!info] Linear Transformation
> A transformation $T : \mathbb{R}^n \rightarrow \mathbb{R}^m$ is a **linear transformation** if it satisfies the following: for all vectors $u, v \in \mathbb{R}^n$ and scalar $c \in \mathbb{R}$

A linear transformation $T : \mathbb{R}^n \rightarrow \mathbb{R}^m$ satisfies:
- $T(0) = 0$
- For any vectors $v_1, v_2, ..., v_k \in \mathbb{R}^n$ and scalars $c_1, ..., c_k \in \mathbb{R}$, we have $T(c_1 v_1 + ... + c_k v_k) = c_1 T(v_1) + ... + c_k T(v_k)$

### Inverse Matrix

For $n \in N = \{ 1, 2, 3, ... \}$, $I_n$ is an $n \times n$ identity matrix and, for any $v \in \mathbb{R}^n$, $I_n v = v$.

> [!info] Inverse Matrix
> Suppose $A$ is an $n \times n$ matrix. If there exists an $n \times n$ matrix $A^{-1}$ satisfying
> 
> $$A A^{-1} = A^{-1} A = I_n$$
> 
> then $A^{-1}$ is the **inverse matrix** of $A$, and we say that $A$ is **invertible**.

> [!tip] Determining if a Matrix is Invertible \#1
> An $n \times n$ matrix $A$ is invertible if and only if $\text{rank}(A) = n$.

> [!tip] Corollary
> Suppose $Ax = b$ has a unique solution for some $b \in \mathbb{R}^n$. Then, $A$ is invertible.

If $Ax = 0$ has only the trivial solution $x = 0$, then $A$ is invertible.

### Gauss-Jordan Technique

> [!info] Gauss-Jordan Technique
> To find $A^{-1}$, we can start with the matrix $[A | I_n]$ and perform a sequence of elementary row operations to obtain $[I_n | A^{-1}]$.

Useful facts: Suppose $A$ and $B$ are invertible $n \times n$ matrices
1. $A^{-1}$ is invertible and $(A^{-1})^{-1} = A$
2. $AB$ is invertible and $(AB)^{-1} = B^{-1} A^{-1}$
3. $A^T$ is invertible and $(A^T)^{-1} = (A^{-1})^T$
4. Suppose $C$ and $D$ are $n \times n$ matrices. If $CD = I_n$, then both $C$ and $D$ are invertible and $D = C^{-1}$. Moreover, if $CD$ is invertible, then both $C$ and $D$ are invertible

### Inverse of 2x2 Invertible Matrix

Suppose $A$ is an invertible 2x2 matrix

$$A = \begin{bmatrix} a & b\\ c & d \end{bmatrix}$$

Then, the inverse is given by

$$A^{-1} = \frac{1}{ad - bc} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$$

### Determinant

> [!info] Determinant
> The **determinant** of an $n \times n$ matrix $A$, denoted by $\text{det}(A)$, is a scalar that can be computed as follows:
> - $n = 1$: If $A = [a]$, then $\text{det}(A) = a$
> - $n = 2$: If $A = \begin{bmatrix} a & b\\ c & d \end{bmatrix}$, then $\text{det}(A) = ad - bc$
> - $n > 2$: Pick a row or column in the matrix, and go through each element in it
> 	- For each element in the row/column selected, eliminate the entire row and column that element is in
> 		- We are finding $C_{i, j} = (-1)^{i + j} M_{i, j}$, the *cofactor* of $A$
> 	- Find the determinant using the remaining elements in the same order they are in (as if they are another matrix)
> 		- This is $M_{i, j}$, the *minor* of $A$
> 	- Multiply the resulting determinant by the current element, and use the following reference matrix for signs (for a 3x3 matrix): $\begin{bmatrix} + & - & + \\ - & + & - \\ + & - & + \end{bmatrix}$
> 		- Alternatively, use the formula $(-1)^{i + j}$, where $0 \leq i \leq n$ and $0 \leq j \leq n$

If $A$ is an $n \times n$ upper/lower triangular matrix, then the determinant is equal to the *product of the diagonal elements*.

> [!info] Elementary Row Operations and Determinants
> Suppose $A$ is an $n \times n$ matrix
> 
> - If $B$ is the matrix obtained by permuting two rows of $A$, then $\text{det}(B) = -\text{det}(A)$
> - If $C$ is the matrix obtained one row of $A$ by a scalar $k$, then $\text{det}(C) = k \cdot \text{det}(A)$
> - If $D$ is the matrix obtained by adding a multiple of any row of $A$ to a different row of $A$, then $\text{det}(D) = \text{det}(A)$ (the determinants are the same)

> [!tip] Determining if a Matrix is Invertible \#2
> Suppose that $A$ is an $n \times n$ matrix. Then, $A$ is invertible if and only if $\text{det}(A) \neq 0$.

Properties of determinants:
- $\text{det}(A^T) = \text{det}(A)$
- If $A$ has a zero row or column, then $\text{det}(A) = 0$
- If either two rows or two columns of $A$ are identical, then $\text{det}(A) = 0$
- $\text{det}(AB) = \text{det}(A) \cdot \text{det}(B)$

### Matrix Similarity

> [!info] Matrix Similarity
> Two $n \times n$ matrices $A$ and $B$ are said to be **similar** if there is an invertible $n \times n$ matrix $P$ such that $B = P^{-1} AP$.

$A \mapsto P^{-1} AP = B$ is called a **similarity transformation** (or **conjugation**).

Suppose $A$ and $B$ are similar:
- $\text{det}(A) = \text{det}(B)$
- $\text{Tr}(A) = \text{Tr}(B)$
- $\text{rank}(A) = \text{rank}(B)$