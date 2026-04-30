---
tags: ENEE_290
created: 2026-4-22
description: 4/22, 4/27 notes (Lecture 23, 24)
---

### Higher Order Differential Equations

$$\frac{d^n y}{dx^y} + p_1(x) \frac{d^{n - 1} y}{dx^{n - 1}} + ... + p_{n - 1}(x) \frac{dy}{dx} + p_n(x) = g(x)$$

> [!tip] Theorem
> If the functions $p_1, ..., p_n$ and $g$ are *continuous* on the open interval $(\alpha, \beta)$, then there exists a *unique* solution $y = \phi(x)$ satisfying the above equation on that interval, and the prescribed initial conditions $y(x_0) = y_0, y'(x_0) = y'_0, ..., y^{(n)} (x_0) = y^{(n)}_0$.

The general solution to the above equation with $g(x) \neq 0$ is given by

$$y(x) = y_c(x) + y_p(x) = (c_1 y_1(x) + ... + c_n y_n(x)) + y_p(x)$$

where $y_p$ is some *particular solution* and $y_1, ..., y_n$ form a [[Second-Order Differential Equations#^7d27c6|fundamental set of solutions]] to the homogenous equation.

### Homogenous Solution with Constant Coefficients

$$a_0 y^{(n)} + a_1 y^{(n - 1)} + ... + a_{n - 1} y' + a_n y = 0$$

We want to guess a solution $y = e^{rx}, r \in C$ and substitute it in the above equation.

Find the characteristic polynomial $Z(r) = a_0 r^n + a_1 r^{n - 1} + ... + a_{n - r} + a_n$ and find its roots.

> [!tip] Real Distinct Roots (Homogenous Equation)
> Suppose $r_1, r_2, ..., r_k$ are *real distinct* roots of the characteristic polynomial. Then,
> 
> $$e^{r_1 x}, e^{r_2 x}, ..., e^{r_k x}$$
> 
> are *linearly independent* solutions to the homogenous equation.

> [!tip] Complex Roots (Homogenous Equation)
> Complex roots occur in conjugate pairs $\lambda \pm j\mu$ when coefficients $a_0, a_1, ..., a_n \in R$
> 
> $$e^{\lambda x} \cos(\mu x), e^{\lambda x} \sin(\mu x)$$
> 
> are solutions of the homogenous equation.

> [!tip] Repeated Roots (Homogenous Equation)
> Suppose that $r_1$ is *real* and repeated $s$ times:
> 
> $$e^{r_1 x}, xe^{r_1 x}, ..., x^{s - 1} e^{r_1 x}$$
> 
> are solutions to the homogenous equation.

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

> [!tip] Linear Independence
> $y_1, ..., y_n$ are linearly independent and form the fundamental set of solutions if $W(y_1, ..., y_n) = \text{det} \left( \begin{bmatrix} y_1&...&y_n \\ \vdots & & \vdots \\ y_1^{(n - 1)} & ... & y_n^{(n - 1)} \end{bmatrix}) \right) \neq 0$

### Method of Undetermined Coefficients

$$a_0 y^{(n)} + a_1 y^{(n - 1)} + ... + a_{n - 1} y' + a_n y = g(x)$$

Assume the above equation has *constant coefficients*.

![[Second-Order Differential Equations#^0af63f|Table of Particular Solutions]]

Find the coefficients by substituting in the differential equation (taking derivatives if needed).

### Method of Variation of Parameters

To use the method of variation of parameters, we first need to solve the corresponding homogenous differential equation and find a fundamental set of solutions.

Suppose $y_1, ..., y_n$ form a fundamental set of solutions of the homogenous equation. We want to find functions $u_1, ..., u_n$ such that

$$y_p(t) = u_1(x) y_1(x) + ... + u_n(x) y_n(x)$$

$$\begin{bmatrix} y_1(x_0) & ... & y_n(x_0) \\ y'_1(x_0) & ... & y'_n(x_0) \\ \vdots & & \vdots \\ y^{(n - 1)}_1 (x_0) & ... & y^{(n - 1)}_n (x_0) \end{bmatrix} \begin{bmatrix} u_1'(x) \\ u_2' (x) \\ \vdots \\ u_n'(x) \end{bmatrix} = \begin{bmatrix} 0 \\ 0\\ \vdots \\ g(x) \end{bmatrix}$$ 

Solve the above matrix for the vector $u'$, then integrate $u_1', u_2', ..., u_n'$ to find the functions $u_1, u_2, ..., u_n$

The solution is given by:

$$u_m'(x) = \frac{g(x) W_m(x)}{W(x)}, m = 1, 2, ..., n$$

$W_m$ is the determinant obtained from $W(y_1, y_2, ..., y_n)$ by replacing the $m$-th column with the column $(0, 0, ..., 0, 1)$.

$$y_p(x) = \sum\limits_{m = 1}^{n} y_m(x) \int^x \frac{g(t) W_m(t)}{W(t)} dt = \sum\limits_{m = 1}^n y_m(x) u_m(x)$$