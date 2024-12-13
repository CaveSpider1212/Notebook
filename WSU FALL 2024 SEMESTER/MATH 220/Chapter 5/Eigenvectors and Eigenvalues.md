---
tags: MATH_220
created: 2024-10-29
description: Chapter 5.1
---

> [!info] Eigenvector and Eigenvalue
> An eigenvector of an $n \times n$ matrix $A$ is a nonzero vector $x$ such that $Ax = \lambda x$ for some scalar $\lambda$. A scalar $\lambda$ is called an eigenvalue of $A$ if there is a nontrivial solution $x$ of $Ax = \lambda x$; such an $x$ is called an eigenvector corresponding to $\lambda$.
> 
> The eigenvector will need to be nonzero or the problem is trivial. The eigenvalue can be zero. If the eigenvalue is zero, we are asking for either the solutions to the homogenous system, all $x$ in Nul$A$, or another equivalent definition.

Eigenvectors can be found using row reduction, but usually eigenvalues can't.

> [!tip] Alternative Equation for Eigenvectors or Eigenvalues
> 
> $$(A - \lambda I)x = 0$$
> 
> Using this equation, we can say that $\lambda$ is an eigenvalue if and only if there is a nontrivial solution to the homogenous system.

> [!info] Eigenspace
> The eigenspace of $A$ corresponding to $\lambda$ is the set of all $x$ such that $(A - \lambda I) = 0$.

> [!tip] Theorem
> The eigenvalues of a triangular matrix are the entries on its main diagonal.

> [!tip] Theorem
> If $v_1, ..., v_r$ are eigenvectors that correspond to distinct eigenvalues $\lambda_1, ..., \lambda_r$ of an $n \times n$ matrix $A$, then the set ${v_1, ..., v_r}$ is linearly independent.