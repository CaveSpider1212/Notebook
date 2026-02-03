---
tags: ENEE_290
created: 2026-2-2
description: 2/2 notes (Lecture 2)
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