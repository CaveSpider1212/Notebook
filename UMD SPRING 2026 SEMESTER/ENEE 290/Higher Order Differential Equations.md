---
tags: ENEE_290
created: 2026-4-22
description: 4/22 notes (Lecture 23)
---

### Higher Order Differential Equations

$$\frac{d^n y}{dx^y} + p_1(x) \frac{d^{n - 1} y}{dx^{n - 1}} + ... + p_{n - 1}(x) \frac{dy}{dx} + p_n(x) = g(x)$$

> [!tip] Theorem
> If the functions $p_1, ..., p_n$ and $g$ are *continuous* on the open interval $(\alpha, \beta)$, then there exists a *unique* solution $y = \phi(x)$ satisfying the above equation on that interval, and the prescribed initial conditions $y(x_0) = y_0, y'(x_0) = y'_0, ..., y^{(n)} (x_0) = y^{(n)}_0$.

The general solution to the above equation with $g(x) \neq 0$ is given by

$$y(x) = y_c(x) + y_p(x) = (c_1 y_1(x) + ... + c_n y_n(x)) + y_p(x)$$

where $y_p$ is some *particular solution* and $y_1, ..., y_n$ form a [[Second-Order Differential Equations#^7d27c6|fundamental set of solutions]] to the homogenous equation.

### Fundamental Set of Solutions

The solutions to the homogenous equation $y_1, ..., y_n$ form a fundamental set of solutions if, for any initial conditions, it is possible to find constants $c_1, ..., c_n$ so that $y(x) = c_1 y_1(x) + ... + c_n y_n(x)$ satisfies the initial conditions

$$y(x_0) = c_1 y_1(x_0) + ... + c_n y_n(x_0) = y_0$$
$$y'(x_0) + c_1 y'_1(x_0) + ... + c_n y'_n(x_0) = y'_0$$
$$...$$
$$y^{(n - 1)}(x_0) = c_1 y^{(n - 1)}_1 (x_0) + ... + c_n y^{(n - 1)}_n(x_0) = y^{(n - 1)}_0$$

The above can be written in matrix form:
$$\begin{bmatrix} y_1(x_0) & ... & y_n(x_0) \\ y'_1(x_0) & ... & y'_n(x_0) \\ \vdots & & \vdots \\ y^{(n - 1)}_1 (x_0) & ... & y^{(n - 1)}_n (x_0) \end{bmatrix} \begin{bmatrix} c_1\\ c_2\\ \vdots \\ c_n \end{bmatrix} = \begin{bmatrix} y_0\\ y'_0 \\ \vdots \\ y^{(n - 1)}_0 \end{bmatrix}$$
$$Mc = y_0$$

Can always be solved for $c_1, ..., c_n$ when $M$ is invertible or when its determinant is nonzero for any given initial conditions.

$\text{det}(M) = W(y_1, ..., y_n)$ is the [[Second-Order Differential Equations#^64a058|Wronskian]].