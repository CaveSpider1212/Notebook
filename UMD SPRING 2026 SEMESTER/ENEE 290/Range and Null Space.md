---
tags: ENEE_290
created: 2026-3-30
description: 3/30, 4/1 notes (Lecture 16, 17)
---

### Range and Null Space of Matrix

> [!info] Range
> Suppose $A$ is an $m \times n$ real matrix in $\mathbb{R}^{m \times n}$. The **range** of $A$, denoted by $\mathcal{R}(A)$, is the set of all vectors in $\mathbb{R}^m$ which can be written as linear combinations of the columns of $A$.
> 
> $$\mathcal{R} (A) = \{ Ax : x \in \mathbb{R}^n \} = \text{span} \{ A_{., 1}, ..., A_{., n} \} \subset \mathbb{R}^m$$

The range $\mathcal{R} (A)$ is a *subspace* of $\mathbb{R}^m$, and its dimension is called the **rank** of $A$, denoted by $\text{rank}(A)$.

$\text{rank} (A)$ represents the number of linearly independent columns of $A$.

The range $\mathcal{R} (A)$ is also called the **column space** of $A$.

> [!info] Null Space
> The **null space** (or **kernel**) of an $m \times n$ matrix $A$, denoted by $\mathcal{N} (A)$, is the set of all vectors $x \in \mathbb{R}^n$ mapped to zero vector by $A$.
> 
> $$\mathcal{N} (A) = \{ x \in \mathbb{R}^n | Ax = 0 \} \subset \mathbb{R}^n$$

The null space is just the solution set to the *homogeneous system* of linear equations ($Ax = 0$).

The null space $\mathcal{N} (A)$ is a *subspace* of $\mathbb{R}^n$.

Useful facts:
1. $\text{rank} (A) = \text{rank} (A^T)$
2. Every row-echelon form of $A$ has the same rank

### Row Space of Matrix

The range of $A^T$ is called the **row space** of $A$, i.e. the set of all vectors in $\mathbb{R}^n$ which can be written as linear combinations of the rows of $A$.

The row space of $A$ is a *subspace* of $\mathbb{R}^n$ whose dimension is equal to the rank of $A$.

### Basis for Range and Row Space

Finding a basis for the row space $\mathcal{R} (A^T)$:

> [!tip] Theorem
> Suppose matrices $A$ and $B$ are row equivalent. Then, $\mathcal{R}(A^T) = \mathcal{R} (B^T)$.

If $B$ is row equivalent to $A$, then $B$ can be obtained from $A$ using reversible elementary row operations, meaning the rows of $B$ can be obtained as linear combinations of the rows of $A$ and vice versa. A basis for the row space of $A$ would be the nonzero rows of $B$.

> [!tip] Theorem
> Suppose that $C$ is a row-echelon form of $A$. Then, the nonzero rows of $C$ are linearly independent.

> [!tip] Finding a Basis for Any Linear Span of Vectors
> The set of nonzero row vectors in a row-echelon matrix $C$ is a basis for $\mathcal{R} (A^T)$.

Finding a basis for the column space/rank $\mathcal{R} (A)$:

> [!tip] Theorem
> Suppose $A$ is an $m \times n$ matrix and $B$ is a row-equivalent row-echelon form of $A$. Then, the set of column vectors of $A$ corresponding to those column vectors containing leading 1's is a basis for $\mathcal{R} (A)$.

### Null Space and Nullity

Finding a basis for the null space $\mathcal{N} (A)$:

> [!info] Nullity
> The dimension of $\mathcal{N} (A)$ is called the **nullity** of $A$, denoted by $\text{nullity} (A)$

If $\text{rank} (A) = r$, then any row-echelon form of $A$ has $r$ leading 1's
- This implies that there are  $r$ bound variables when finding the solution set
- This suggests that there are $n - r$ free variables in the solution of the homogenous system $Ax = 0$

> [!tip] Rank-Nullity Theorem
> Suppose that $A$ is an $m \times n$ matrix. Then,
> 
> $$\text{rank} (A) + \text{nullity} (A) = n$$
> 
> $\text{rank} (A)$: number of bound variables
> $\text{nullity} (A)$: number of free variables
> $n$: number of columns or unknowns

### Summary for Homogenous Systems

> [!tip]
> Suppose $A$ is an $m \times n$ matrix, and consider the homogenous system $Ax = 0$
> 1. If $\text{rank}(A) = n$, then $\mathcal{N}(A) = 0$, i.e. $Ax = 0$ has only the trivial solution $0$ because $\text{nullity}(A) = 0$
> 2. If $\text{rank}(A) = r < n$, then $\text{nullity}(A) \geq 1$ and, hence, there are infinitely many solutions to $Ax = 0$

### Summary for Nonhomogeneous Linear Systems

> [!tip]
> Suppose $A$ is an $m \times n$ matrix, and consider the linear system $Ax = b$
> 
> 1. If $b \notin \mathcal{R} (A)$, then there is no solution (and the system is said to be *inconsistent*)
> 2. If $b \in \mathcal{R} (A)$, the system has a solution (and is said to be *consistent*)
> 	1. There is a unique solution if and only if $\text{rank}(A) = n$
> 	2. There are infinitely many solutions if and only if $\text{rank}(A) < n$

> [!tip] Theorem
> Let $A$ be an $m \times n$ matrix. If $\text{rank}(A) = r < n$ and $b \in \mathcal{R}(A)$, then all solutions to $Ax = b$ are of the form:
> 
> $$x = c_1 x_1^0 + ... + c_{n - r} x_{n - r}^0 + x_p = x_h + x_p$$
> 
> where $x_p$ is *any* particular solution to $Ax = b$, and $\{ x_1^0, ..., x_{n - r}^0 \}$ is a basis for the null space $\mathcal{N}(A)$.