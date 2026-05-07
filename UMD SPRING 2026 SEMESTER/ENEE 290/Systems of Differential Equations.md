---
tags: ENEE_290
created: 2026-4-29
description: 4/29 notes (Lecture 25)
---

### System of Differential Equations

Consider the following system of first-order linear differential equations

$$x_1' = p_{1, 1} (t) x_1 + p_{1,2}(t) x_2 + ... + p_{1,n} x_n + g_1(t)$$
$$x'_2 = p_{2,1}(t)x_1 + p_{2,2}(t) x_2 + ... + p_{2,n}x_n + g_2(t)$$
$$\vdots$$
$$x_n' = p_{n,1}(t) x_1 + p_{n,2}(t) x_2 + ... + p_{n,n} x_n + g_n(t)$$

The system is *homogenous* if $g_1 = g_2 = ... = g_n = 0$. Otherwise, it is *non-homogenous*.

A solution of the above system is an $n$-tuple of functions $(x_1, x_2, ..., x_n)$ which satisfies the differential equations in the system.

> [!info] Matrix Equation
> $$\dot{x} = Px + g$$
> 
> where $\dot{x} = \begin{bmatrix} x_1' & ... & x_n' \end{bmatrix}^T$ is the first derivative with respect to time and $x = \begin{bmatrix} x_1 & ... & x_n \end{bmatrix}^T, g = \begin{bmatrix} g_1& ... & g_n \end{bmatrix}^T, P = \begin{bmatrix} p_{i,j}; i, j = 1, ..., n \end{bmatrix}$.

### Existence and Uniqueness of a Solution

> [!tip] Existence and Uniqueness Theorem
> Suppose that the functions $p_{i, j}, i, j = 1, ..., n$ and $g_i, i = 1, ..., n$ are continuous over the interval $I = (\alpha, \beta)$. Then, given initial conditions $x_1(t_0) = x_0^1, x_2(t_0) = x_0^2, ..., x_n(t_0) = x_0^n, t_0 \in I$, there is a unique solution $(x_1, x_2, ..., x_n)$ that satisfies the system of equations and the given initial conditions.

We need $n$ initial conditions, one for each function, for the uniqueness of a solution.

Initial conditions can be written as $x(t_0) = x_0$.

### General Solutions

> [!info] General Solutions
> The general solution to a system of differential equations is given by
> 
> $$x(t) = x_c(t) + x_p(t)$$
> 
> $x_p$: any particular solution satisfying the system of equations
> $x_c$: complementary solution to the homogenous equation $\dot{x} = Px$

### Homogenous System

Suppose that $x_1$ and $x_2$ are two solutions to the homogenous equation $\dot{x} = Px$. Then, so is any linear combination of $x_1$ and $x_2$.

> [!info] Linearly Dependent
> See [[Second-Order Differential Equations#^3dca20]]

> [!tip] Theorem
> Suppose that $x_1, x_2, ..., x_n$ are $n$ solutions of the homogenous equation on an open interval $I = (\alpha, \beta)$ and that $P(t)$ is continuous on $I$. Define
> 
> $$W = W(x_1, ..., x_n) = \text{det}(\begin{bmatrix} x_1&x_2&...&x_n \end{bmatrix})$$
> 
> Then,
> 1. If $x_1, x_2, ..., x_n$ are *linearly dependent* on $I$, then $W = 0$ for all $t \in I$.
> 2. If $x_1, x_2, ..., x_n$ are *linearly independent* on $I$, then $W \neq 0$ for all $t \in I$.

> [!tip] Theorem
> Suppose $x_1, x_2, ..., x_n$ are $n$ *linearly independent* solutions of the homogenous equation on an interval $I$, where $P(t)$ is continuous over the interval. Then, any solution of the homogenous equation can be expresses as a linear combination of $x_1, x_2, ..., x_n$.
> 
> $$x(t) = c_1 x_1(t) + ... + c_n x_n(t), \forall t \in I$$
> 
> for some scalars $c_1, ..., c_n$.
> 
> This forms the **fundamental set of solutions**.

The coefficients $\mathbf{c} = \begin{bmatrix} c_1&...&c_n \end{bmatrix}^T$ must be a solution to $x(t_0) = c_1 x_1(t_0) + ... + c_n x_n(t_0) = X(t_0) c = b$

$$\mathbf{c} = X(t_0)^{-1} \mathbf{b}$$