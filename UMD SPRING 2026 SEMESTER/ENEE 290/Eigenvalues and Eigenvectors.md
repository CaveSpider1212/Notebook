---
tags: ENEE_290
created: 2026-4-8
description: 4/8, 4/13, 4/20 notes (Lecture 19, 20, 22)
---

### Eigenvalues and Eigenvectors

> [!info] Eigenvector/Eigenvalue
> Suppose $A$ is an $n \times n$ matrix. A nonzero *column vector* $v \in R^n$ is a **right eigenvector** of $A$ if there is some constant $\lambda \in C$ such that $Av = \lambda v$.
> 
> The constant $\lambda$ is called a **(right) eigenvalue**.
> 
> A left eigenvector is the same as a right eigenvector but with a *row vector* instead.

Eigenvalues are also called *characteristics values*.

Eigenvectors are usually referred to as a "right eigenvector" if not specified.

> [!tip] Finding Eigenvalues and Eigenvectors
> If $\lambda$ is an eigenvalue and $v$ is a right eigenvector:
> 
> $$(A - \lambda I) v = 0$$

> [!info] Characteristic Polynomial and Characteristic Equation
> The polynomial $p(\lambda)$ defined by $\text{det} (A - \lambda I)$ is called the **characteristic polynomial** of $A$.
> 
> The equation $p(\lambda) = 0$ is called the **characteristic equation** of $A$.

The eigenvalues of $A$ are the *roots of the characteristic polynomial* (i.e. the solutions to the characteristic equation).

Once the eigenvalues $\lambda_i, i = 1, ..., n$ are found, then the equation $(A - \lambda_i I) v_i = 0$ can be solved to find all eigenvectors $v_i$ corresponding to each eigenvalue using the equation $Av = \lambda v$

### Eigenspace

> [!info] Eigenspace
> For a given eigenvalue $\lambda_i$ of $A$ (an $n \times n$ matrix), let $E_i$ be the set of all vectors $v$ satisfying $Av = \lambda_i v$. Then, $E_i$ is called the **eigenspace** of $A$ corresponding to the eigenvalue $\lambda_i$.

For each $i$, $E_i$ is a subspace of $C^n$.

If $n_i = \text{dim} (E_i)$, then $1 \leq n_i \leq m_i$, where $m_i$ is the multiplicity of $\lambda_i$.

Sometimes $m_i$ and $n_i$ are called the algebraic and geometric multiplicities of $\lambda_i$, respectively.

> [!tip] Theorem
> Eigenvectors corresponding to *distinct* eigenvalues are linearly independent.

> [!info] Non-defective
> Suppose that $\text{dim}(E_i) = m_i$ for all $i = 1, ..., k$, where $m_i$ is the multiplicity of $\lambda_i$. Then, $A$ is said to be **non-defective** and to have a *complete set of eigenvalues)*

^699211

When $A$ is non-defective, we can find a basis for $E_i$ with $m_i$ vectors. Therefore, since the eigenvectors associated with distinct eigenvalues are linearly independent, we can find a basis for $C^n$. Such a basis is called an **eigenbasis** of $A$.

Relationship between determinant and eigenvalues:
1. $\text{det}(A) = \prod_{i = 1}^{k} \lambda_i ^{m_i}$ (product of eigenvalues)
2. $\sum\limits_{i = 1}^{k} m_i \cdot \lambda_i = \sum\limits_{i = 1}^{n} a_{i, i} = Tr(A)$ (sum of eigenvalues)

### Matrix Decomposition

> [!info] Diagonalization
> An $n \times n$ matrix is said to be **diagonalizable** if it is *similar to a diagonal matrix*.

> [!tip] Theorem
> Suppose $A$ and $B$ are similar $n \times n$ matrices. Then, $A$ and $B$ have the same eigenvalues (along with the same trace and determinant).

> [!tip] Diagonalizable
> An $n \times n$ matrix $A$ is diagonalizable if and only if $A$ is non-defective.
> 
> If $A$ has $n$ distinct eigenvalues, it is diagonalizable.

> [!info] Eigenvalue Decomposition
> Suppose that an $n \times n$ matrix $A$ is diagonalizable and that $v_1, ..., v_n$ are $n$ linearly independent eigenvectors. Then, the factorization
> 
> $$A = S \Lambda S^{-1}$$
> 
> where $S = \begin{bmatrix} v_1&...&v_n \end{bmatrix}$ and $\Lambda$ is a diagonal matrix with corresponding eigenvalues $\lambda_i$ as the $i$-th diagonal element, is called the **spectral decomposition** or **eigenvalue decomposition**.

### Symmetric Matrices

See [[Matrices#^f4413d]].

Useful facts:
- Eigenvalues of a symmetric real matrix are real
- Eigenvectors of a symmetric real matrix corresponding to two distinct eigenvalues are *orthogonal*
- $A$ is non-defective and has a complete set of *orthonormal eigenvectors*

### Orthogonal Matrix

> [!info] Orthogonal Matrix
> A real $n \times n$ matrix is said to be **orthogonal** if $A^{-1} = A^T$.

> [!tip] Spectral Decomposition with Orthonormal Eigenvectors
> Assume $S$ contains $n$ distinct orthonormal eigenvectors.
> 
> $$A = S \Lambda S^T = \sum\limits_{i = 1}^{n} \lambda_i v_i v_i^T$$

### Positive Semidefinite and Positive Definite Matrices

> [!info] Positive Semidefinite
> An $n \times n$ symmetric matrix $A$ is said to be **positive semidefinite** if, for all $x \in R^n$,
> 
> $$x^T Ax \geq 0$$

1. A real symmetric matrix is positive semidefinite if and only if its eigenvalues are real and nonnegative
2. Determinant is nonnegative
3. Trace is nonnegative

> [!info] Positive Definite
> An $n \times n$ symmetric matrix $A$ is said to be **positive definite** if, for all nonzero vector $x \in R^n \backslash \{ 0 \}$,
> 
> $$x^T Ax > 0$$

1. A real symmetric matrix is positive semidefinite if and only if its eigenvalues are *strictly positive*
2. Determinant is *strictly positive* and the matrix is invertible
3. Trace is strictly positive

### Principal Component Analysis (PCA)

Centered dataset: $Y = X - 1x_{\text{avg}}$

Covariance matrix: Real, positive semidefinite matrix

$$C = \frac{1}{n - 1} Y^T Y = VDV^T \in S^m_+$$

The columns of $V$ are eigenvectors associated with $m$ eigenvalues and form an *orthonormal basis* for $R^m$.

Approximate samples using: $y_i^r = \sum\limits_{k = 1}^{r} \langle y_i, v_k \rangle v_k = \sum\limits_{k = 1}^{r} \hat{y}_{i, k} v_k$