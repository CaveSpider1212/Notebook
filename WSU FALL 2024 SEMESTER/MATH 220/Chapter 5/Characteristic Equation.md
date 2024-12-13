---
tags: MATH_220
created: 2024-10-31
description: Chapter 5.2
---

> [!info] The Characteristic Equation
> The scalar equation det$(A - \lambda I) = 0$ is called the characteristic equation of $A$.
> 
> A scalar $\lambda$ is an eigenvalue of an $n \times n$ matrix $A$ if and only if $\lambda$ satisfies the characteristic equation det$(A - \lambda I) = 0$.

> [!info] Similarity
> If $A$ and $B$ are $n \times n$ matrices, then $A$ is similar to $B$ if there is an invertible matrix $P$ such that $P^{-1}AP = B$, or, equivalently $A = PBP^{-1}$. Changing $A$ into $P^{-1}AP$ is called a similarity transformation.
> 
> Note: You can define $P^{-1} = Q$, so $Q^{-1}BQ = A$ which implies $B$ is also similar to $A$.

> [!tip] Theorem
> If $n \times n$ matrices $A$ and $B$ are similar, then they have the same characteristic polynomial and hence the same eigenvalues (with the same multiplicities).