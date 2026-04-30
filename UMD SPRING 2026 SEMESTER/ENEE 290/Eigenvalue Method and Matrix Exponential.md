---
tags: ENEE_290
created: 2026-4-29
description: 4/29 notes (Lecture 25)
---

### Eigenvalue Method for Linear Systems

Consider a *homogenous* system with *constant coefficients* $\dot{x} = Ax$. We want to find $n$ linearly independent solutions $x_1, ..., x_n$.

Let $\lambda_1, ..., \lambda_n$ be $n$ eigenvalues of $A$ and $v_1, ..., v_n$ be the corresponding eigenvectors.

Define $x_i(t) = v_i e^{\lambda_i t}, i = 1, ..., n$

$$\dot{x}_i(t) = \lambda_i v_i e^{\lambda_i t} = Ax(t), i = 1, ..., n$$

$x_1, ..., x_n$ are solutions to the homogenous system.

When $A$ is [[Eigenvalues and Eigenvectors#^699211|non-defective]], we can find $n$ linearly independent eigenvectors $v_1, ..., v_n$ and $n$ linearly independent solutions to the homogenous system $x_i(t) = v_i e^{\lambda_i t}, i = 1, ..., n$, from the eigenvalues and linearly independent eigenvectors.