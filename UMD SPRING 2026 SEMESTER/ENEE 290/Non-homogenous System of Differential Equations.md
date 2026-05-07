---
tags: ENEE_290
created: 2026-5-4
description: 5/4, 5/6 notes (Lecture 26, 27)
---

### Non-homogenous System

Consider the non-homogenous system of first-order linear differential equations:

$$\mathbf{\dot{x}} = \mathbf{Ax} + \mathbf{g}$$

where $A \in R^{n \times n}$ and $g$ is a continuous vector-valued function.

General solution: $x(t) = x_c(t) + x_p(t)$

We want to find a *particular solution* $x_p$, using either the *method of undetermined coefficients* or *method of variation of parameters*.

### Method of Undetermined Coefficients

Suppose the functions in $\mathbf{g}$ are products of polynomials, exponentials, or sinusoidal functions.

Guess the general form of a particular solution $\mathbf{x}_p$ and determine the *unknown coefficient vectors*.

### Method of Variation of Parameters

We want to find a particular solution of the nonhomogenous system

$$\mathbf{\dot{x}} = \mathbf{Px} + \mathbf{g}$$

The complementary solution can be written as $x_c(t) = \Phi(t) c$, where $c$ is the coefficient vector.

$$x_p(t) = \Phi(t) u(t) = u_1(t) x_1(t) + ... + u_n(t) x_n(t)$$

where $u(t) = \begin{bmatrix} u_1(t)&...&u_n(t) \end{bmatrix}^T$

To find $u(t)$, we need to introduce some conditions satisfying

$$\dot{x}_p(t) = \dot{\Phi}(t) u(t) + \Phi(t) \dot{u}(t)$$

We get the final equation

$$\dot{\Phi}(t) \mathbf{u}(t) + \Phi(t) \mathbf{\dot{u}}(t) = \mathbf{P}(t) \Phi(t) \mathbf{u}(t) + \mathbf{g}(t)$$

This tells us:

$$\mathbf{u}(t) = \int^t \Phi(s)^{-1} \mathbf{g}(s) ds$$

$$x_p(t) = \Phi(t) \mathbf{u}(t) = \Phi(t) \int^t \Phi(s)^{-1} \mathbf{g}(s) ds$$

Initial value problem with initial conditions $x(t_0) = \mathbf{b}$:

$$x(t) = \Phi(t) \Phi(t_0)^{-1} \mathbf{b} + \Phi(t) \int_{t_0}^{t} \Phi(s)^{-1} \mathbf{g}(s) ds$$