---
tags: ENEE_290
created: 2026-4-29
description: 4/29, 5/4 notes (Lecture 25, 26)
---

### Eigenvalue Method for Linear Systems

Consider a *homogenous* system with *constant coefficients* $\dot{x} = Ax$. We want to find $n$ linearly independent solutions $x_1, ..., x_n$.

Let $\lambda_1, ..., \lambda_n$ be $n$ eigenvalues of $A$ and $v_1, ..., v_n$ be the corresponding eigenvectors.

Define $x_i(t) = v_i e^{\lambda_i t}, i = 1, ..., n$

$$\dot{x}_i(t) = \lambda_i v_i e^{\lambda_i t} = Ax(t), i = 1, ..., n$$

$x_1, ..., x_n$ are solutions to the homogenous system.

When $A$ is [[Eigenvalues and Eigenvectors#^699211|non-defective]], we can find $n$ linearly independent eigenvectors $v_1, ..., v_n$ and $n$ linearly independent solutions to the homogenous system $x_i(t) = v_i e^{\lambda_i t}, i = 1, ..., n$, from the eigenvalues and linearly independent eigenvectors.

When initial conditions $x(t_0) = b$ are given, $c = X(t_0)^{-1} b$ and $x(t) = X(t) X(t_0)^{-1} b$.

### Matrix Exponential

> [!info] Matrix Exponential
> Suppose that $A$ is an $n \times n$ matrix. Then, the exponential of matrix $A$ is the $n \times n$ matrix given by
> 
> $$e^A = I + A + \frac{A^2}{2!} + ... + \frac{A^n}{n!} + ... = \sum\limits_{k \in Z_+} \frac{A^k}{k!} = \lim_{K \to \infty} \sum\limits_{k = 0}^{K} \frac{A^k}{k!}$$

$e^0 = I$

> [!info] Nilpotent
> A matrix $A$ with vanishing power $A^n = 0$ for some finite $n$ is said to be **nilpotent**.

- Useful facts
	- Suppose that $A$ and $B$ are two $n \times n$ matrices that *commute*, i.e., $AB = BA$. Then, $e^{A + B} = e^A e^B$
	- For any $n \times n$ matrix $A$, $(e^A)^{-1} = e^{-A}$
		- Existence of the inverse is always guaranteed, meaning $e^A$ is always invertible and hence has $n$ linearly independent columns (with rank $n$)

Scalar multiplication: Suppose $A$ is an $n \times n$ matrix and $t \in R$. Then,

$$e^{At} = \sum\limits_{k = 0}^{\infty} \frac{A^k t^k}{k!} = I + At + \frac{A^2 t^2}{2!} + ...$$

converges for any $n \times n$ matrix and fixed $t$.

### Matrix Exponential Method

> [!tip] Theorem
> Suppose $A$ is an $n \times n$ matrix. Then, the unique solution of the initial value problem
> 
> $$\dot{x} = Ax, x(0) = x_0$$
> 
> is given by $x(t) = e^{At} x_0$

$$e^{At} = \hat{X}(t) \hat{X}(0)^{-1}$$

### Computing Matrix Exponential

> [!tip] Cayley-Hamilton Theorem
> Suppose $A$ is an $n \times n$ matrix.
> 
> Recall that the [[Eigenvalues and Eigenvectors#^5ba1e7|characteristic polynomial]] of a matrix $A$ is given by $p(\lambda) = det(A - \lambda I) = (-1)^n \lambda^n + c_1 \lambda^{n - 1} + ... + c_{n - 1} \lambda + c_n$, and eigenvalues $\lambda_i, i = 1, ..., n$ satisfy $p(\lambda_i) = 0, i = 1, ..., n$.
> 
> The matrix $A$ satisfies
> 
> $$p(A) = (-1)^n A^n + c_1 A^{n - 1} + ... + c_{n - 1}A + c_n I = 0$$