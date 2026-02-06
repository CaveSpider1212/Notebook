---
tags: ENEE_290
created: 2026-2-2
description: 2/2, 2/4 notes (Lecture 2, 3)
---

### What are Differential Equations?

**Differential equations** involve one or more derivatives of an unknown function, where there is both an independent variable and an unknown function or dependent variable

$$\frac{dy}{dx} = xy$$

**Ordinary differential equations** are when the unknown function depends only on a *single* independent variable (like the example above).

The **order** of a differential equation is the order of the *highest derivative*.

> [!info] Linear Differential Equations
> **Linear differential equations** are differential equations that contain no products of terms involving the dependent variable and can be written in the form
> 
> $$a_0 (x) y^{(n)} + a_1 (x) y^{(n - 1)} + ... + a_n (x) y = F(x)$$
> 
> where $a_0, a_1, ..., a_n$ and $F$ are functions of $x$ only.

### General and Particular Solutions

A **general solution** includes all possible solutions and typically includes arbitrary constants.

A **particular solution** is a unique solution derived from the general solution by applying specific initial or boundary conditions to determine the exact values of the arbitrary constants.

### First-Order Differential Equations

> [!info] First-Order Differential Equation
> $$y' = f(x, y)$$
> 
> where $f$ is a given function of two variables.
> 
> Any differentiable function $y = u(x)$ satisfying the above equation is called a **solution**.
> 
> The existence of a solution is not guaranteed, but there could also be more than one solution.

We want to look for $y = u(x)$ whose derivative satisfies $y' = f(x)$, meaning $u$ is the antiderivative of $f$, so:

$$y = u(x) = \int^{x} f(t) dt + C$$

### First-Order Linear Differential Equations

There is no general method to find solutions for regular first-order differential equations (as shown above), but there are ways to find solutions for first-order *linear* differential equations

> [!info] First-Order Linear Differential Equation
> $f(x, y)$ depends linearly on dependent variable $y$
> 
> $$y' + p(x) y = g(x)$$
> 
> where $p$ and $g$ are given continuous functions on some interval $(a, b)$.

##### Case \#1: $p(x) = a \neq 0$ and $g(x) = 0$

$$y' + ay = 0 \leftrightarrow y' = -ay$$

The general solution is given by $y = c \times e^{-ax}$, where $c$ is some constant.

To obtain a particular solution, we need to specify an *initial condition* given by a pair $(x_0, y_0)$ such that $y_0 = u(x_0) = c \times e^{-ax_0}$

##### Case \#2: $p(x) = a \neq 0$

$$y = e^{-ax} \int^{x} e^{at} g(t) dt + Ce^{-ax}$$

##### Case \#3 (General case): $y' + p(x)y = g(x)$

$$y = \mu(x)^{-1} (\int^{x} \mu(t) g(t) dt + C)$$
$$\mu(x) = e^{\int^{x} p(t) dt}$$

### Uniqueness of Solution

^7633b7

> [!tip] Uniqueness of a Solution Theorem
> Suppose that the functions $p$ and $g$ are continuous on an open interval $(a, b)$ containing $x_0$. Then, there exists a *unique* solution $y = u(x)$ that satisfies the equation
> 
> $$y' + p(x)y = g(x)$$
> 
> for $x \in (a, b)$ and the initial condition $y(x_0) = y_0$

^779d7e

### Separable Equations

Convenient to write $y' = f(x, y)$ in the form

$$M(x, y) + N(x, y) \frac{dy}{dx} = 0$$
$$M(x) + N(y) \frac{dy}{dx} = 0$$
$$M(x) dx = -N(y) dy$$

If we can find the antiderivatives of $M$ and $N$, the solution can be obtained in the implicit form $H_1 (x) + H_2 (y) = C$ without derivatives

- Steps:
	- Rewrite differential equation in the form $M(x) dx = -N(y) dy$
	- Integrate both sides of the equation written in the above form
	- Substitute the given initial condition to determine the arbitrary constant
	- Solve for $y$ to determine the solution, and make sure it satisfies the initial condition

> [!info] General Solution of Separable Equations
> $$\int N(y) dy = \int M(x) dx + C$$
> $$\int_{x_0}^{x} M(t) dt = \int_{y_0}^{y} -N(t) dt + C$$