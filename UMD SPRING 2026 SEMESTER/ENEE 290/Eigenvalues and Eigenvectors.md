---
tags: ENEE_290
created: 2026-4-8
description: 4/8 notes (Lecture 19)
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