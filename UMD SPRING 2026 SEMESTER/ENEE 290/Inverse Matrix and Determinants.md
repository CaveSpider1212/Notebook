---
tags: ENEE_290
created: 2026-4-1
description: 4/1 notes (Lecture 17)
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

> [!tip] Theorem
> An $n \times n$ matrix $A$ is invertible if and only if $\text{rank}(A) = n$.

> [!tip] Corollary
> Suppose $Ax = b$ has a unique solution for some $b \in \mathbb{R}^n$. Then, $A$ is invertible.

If $Ax = 0$ has only the trivial solution $x = 0$, then $A$ is invertible.

### Gauss-Jordan Technique

> [!info] Gauss-Jordan Technique
> To find $A^{-1}$, we can start with the matrix $[A | I_n]$ and perform a sequence of elementary row operations to obtain $[I_n | A^{-1}]$.