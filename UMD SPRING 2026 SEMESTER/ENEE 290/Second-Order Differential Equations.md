---
tags: ENEE_290
created: 2026-2-4
description: 2/4, 2/9 notes (Lecture 3, 4)
---

$$y'' = f(x, y, y')$$ 
$$y_0 = y(x_0)$$
$$y'_0 = y'(x_0)$$

The same [[First-Order Differential Equations#^779d7e|Uniqueness Theorem]] applies here.

### Homogenous Equation

$$y'' + p(x) y' + q(x) y = 0$$

> [!tip] Superposition Principle
> Suppose $y = y_1 (x)$ and $y = y_2 (x)$ are solutions of the above equation. Then, the linear combination
> 
> $$y = c_1 y_1(x) + c_2 y_2(x)$$
> 
> where $c_1$ and $c_2$ are arbitrary constants, is a solution as well.

The superposition principle suggests that infinitely many solutions of the above equation can be constructed as linear combinations of two solutions.

The superposition principle doesn't hold in general for non-linear differential equations.

Two solutions $y_1$ and $y_2$ are said to form a *fundamental set of solutions* if *every* solution of $y'' + p(x) y' + q(x) y = 0$ can be expressed as a linear combination of $y_1$ and $y_2$.

> [!tip] Theorem
> Suppose the functions $p$ and $q$ are continuous on the interval $(a, b)$ and $y_1$ and $y_2$ are solutions of the above equation satisfying
> 
> $$y_1(x) y_2'(x) - y_1'(x) y_2(x) \neq 0$$
> 
> for all $x \in (a, b)$.
> 
> Then, any solution of $y'' + p(x) y' + q(x) y = 0$ on the interval $(a, b)$ can be written uniquely as a linear combination of $y_1$ and $y_2$.
> 
> This means every solution $y = u(x)$ of the above homogenous equation can be written as a linear combination of $y_1$ and $y_2$.
> 
> This also means that either $y_1(x) y_2'(x) - y_1'(x) y_2(x) \neq 0$ or $y_1(x) y_2'(x) - y_1'(x) y_2(x) = 0$ is true for all $x \in (a, b)$.

When $y_1$ and $y_2$ satisfy the above condition, the linear combination $y = c_1 y_1 + c_2 y_2$ is called the *general solution* of the above homogenous equation.

> [!tip] Theorem
> Suppose the functions $p$ and $q$ are continuous on interval $(a, b)$. Then, there always exists a fundamental set of solutions on the interval $(a, b)$.

> [!info] Linearly Dependent
> Two functions $f$ and $g$ are said to be **linearly dependent** on an interval $(a, b)$ if there exist two constants $k_1$ and $k_2$, at least one of which is not equal to zero, such that 
> 
> $$k_1 f(x) + k_2 g(x) = 0$$
> 
> for all $x \in (a, b)$.
> 
> Two functions $f$ and $g$ are said to be **linearly independent** on an interval if they are not linearly dependent on it.

> [!tip] Wronskian
> Suppose $f$ and $g$ are differentiable functions. If the Wronskian
> 
> $$W(f, g) := f \cdot g' - f' \cdot g$$
> 
> is not identically zero on $(a, b)$, then $f$ and $g$ are linearly independent on the interval $(a, b)$. Furthermore, if $f$ and $g$ are linearly dependent, then $W(f, g)$ is identically zero on $(a, b)$.
> 
> Suppose that $y_1$ and $y_2$ are solutions of the above homogenous equation with $p$ and $q$ continuous on $(a, b)$. Then, $y_1$ and $y_2$ are linearly dependent *if and only if* $W(y_1, y_2)$ is identically zero on $(a, b)$. In addition, $y_1$ and $y_2$ are linearly independent on $(a, b)$ *if and only if* $W(y_1, y_2)$ is not identically zero, i.e. there exists some $x_0 \in (a, b)$ such that $W(y_1, y_2)(x_0) \neq 0$.

> [!info] Summary of Second-Order Homogenous Differential Equations
> Suppose that $y_1$ and $y_2$ are solutions of
> 
> $$y'' + p(x) y' + q(x) y = 0$$
> 
> where $p$ and $q$ are continuous on interval $(a, b)$. Then, the following four statements are equivalent.
> 
> 1. $y_1$ and $y_2$ form a fundamental set of solutions on $(a, b)$
> 2. $y_1$ and $y_2$ are linearly independent on $(a, b)$
> 3. $W(y_1, y_2)(x_0) \neq 0$ for some $x_0 \in (a, b)$
> 4. $W(y_1, y_2)(x) \neq 0$ for all $x \in (a, b)$

### Finding Solutions

$L[y] = (aD^2 + bD + c)[y] = ay'' + by' + c' = 0$
$y = e^{rx}$

To find the solutions of a second-order homogenous equation (shown above), find the solutions (values of $r$) that make $ar^2 + br + c = 0$ (called the characteristic equation) true using the quadratic formula.

$$r_1 = \frac{-b + \sqrt{b^2 - 4ac}}{2a}$$
$$r_2 = \frac{-b - \sqrt{b^2 - 4ac}}{2a}$$

##### Case 1: $b^2 > 4ac$, $r_1 > r_2$

$$y_1 = e^{r_1 x}$$
$$y_2 = e^{r_2 x}$$

The general solution is given by

$$y = c_1 e^{r_1 x} + c_2 e^{r_2 x}$$

> [!example]
> $y'' + 5y' + 6y = 0$, $y(0) = 0$, $y'(0) = 1$
> 
> Characteristic equations: $r^2 + 5r + 6 = (r + 2) (r + 3) = 0$
> 
> $r_1 = -2$, $r_2 = -3$
> 
> General solution: $y = c_1 e^{-2x} + c_2 e^{-3x}$
> 
> Initial conditions:
> $y(0) = c_1 + c_2 = 0$
> $y'(0) = -2c_1 - 3c_2 = 1$
> $c_1 = 1$, $c_2 = -1$
> 
> Solution: $y = e^{-2x} - e^{-3x}$

##### Case 2: $b^2 = 4ac$, $r = r_1 = r_2 = -\frac{b}{2a}$

The general solution is

$$y = c_1 e^{rx} + c_2 x e^{rx}$$

##### Case 3: $b^2 < 4ac$

$$\lambda = -\frac{b}{2a}$$
$$$\mu = \frac{\sqrt{4ac - b^2}}{2a}$$

$$y_1 = e^{\lambda x} (\cos(\mu x) + j \sin(\mu x))$$
$$y_2 = e^{\lambda x} (\cos(\mu x) - j \sin(\mu x))$$

The general solution is

$$y = c_1 e^{(\lambda + j \mu) x} + c_2 e^{(\lambda - j \mu) x}$$

$$y(x) = c_1 e^{\lambda x} \cos(\mu x) + c_2 e^{\lambda x} \sin(\mu x)$$

### Method of Reduction of Order

If we know one solution, we can find the second linearly independent solution by using the **method of reduction of order**.

We could determine a function $v$ such that $y = v \cdot y_1$ is a solution to $y'' + p(x) y' + q(x) y = 0$.

$$v'(2 y'_1 + py_1) + v'' y_1 = 0$$

Integrate the above equation to get $v$ and substitute it into $y = v \cdot y_1$ along with $y_1$ (which is already known) to get $y$, the second solution.

### Non-homogenous Problem

> [!tip] Theorem
> Suppose that $y_p$ is a solution of the *non-homogenous* linear differential equation $y'' + p(x) y' + q(x) y = g(x)$. Then, any solution $y = u(x)$ of that can be expressed as
> 
> $$u(x) = y_p(x) + c_1 y_1(x) + c_2 y_2(x)$$
> 
> where $y_1$ and $y_2$ are linearly independent solutions of the corresponding *homogenous* equation.

The above linear combination is the *general solution* of $y'' + p(x) y' + q(x) y = g(x)$.

The general solution of the homogenous equation is often called the **complementary solution** and is denoted by $y_c$.

A solution of the non-homogenous equation, $y_p$, is called a **particular solution**.

The general solution is $y = y_c + y_p$.