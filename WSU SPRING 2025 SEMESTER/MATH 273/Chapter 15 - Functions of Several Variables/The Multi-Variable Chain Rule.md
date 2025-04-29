---
tags: MATH_273
created: 2025-2-13
description: Lesson 15.4
---

The "regular" chain rule: If $y = f(g(x))$, then $y = f(u)$ and $u = g(x)$, and $\frac{dy}{dx} = \frac{du}{dx} \cdot \frac{dy}{du}$.

> Now, suppose $z = f(x, y)$ and $x = g(t)$, $y = h(t)$:
> 
> ![[2.13.25 Chain 1.png]]
> 
> $$\frac{dz}{dt} = \frac{dx}{dt} \cdot \frac{\partial z}{\partial x} + \frac{dy}{dt} \cdot \frac{\partial z}{\partial y}$$

> What if $w = f(x, y, z)$, $x = g(s, t)$, $y = h(s, t)$, $z = k(s, t)$?
> 
> ![[2.13.25 Chain 2.png]]
> 
> $$\frac{\partial w}{\partial s} = \frac{\partial x}{\partial s} \cdot \frac{\partial w}{\partial x} + \frac{\partial y}{\partial s} \cdot \frac{\partial w}{\partial y} + \frac{\partial z}{\partial s} \cdot \frac{\partial w}{\partial z}$$
> 
> $$\frac{\partial w}{\partial t} = \frac{\partial x}{\partial t} \cdot \frac{\partial w}{\partial x} + \frac{\partial y}{\partial t} \cdot \frac{\partial w}{\partial y} + \frac{\partial z}{\partial t} \cdot \frac{dw}{dz}$$

> [!example]
> Find $\frac{dz}{dt}$ if $z = x\sin(y)$, $x = t^2$, $y = 4t^3$.
> 
> $\frac{dz}{dt} = \frac{\partial x}{\partial t} \cdot \frac{\partial z}{\partial x} + \frac{\partial y}{\partial t} \cdot \frac{\partial z}{\partial y}$
> $\hspace{6.5mm} = 2t \cdot \sin(y) + 12t^2 \cdot x\cos(y)$

> [!example]
> Find $\frac{dz}{dt}$ if $z = (x + 2y)^{10}$, $x = \sin^2(t)$, $y = (3t + 4)^5$.
> 
> $\frac{dz}{dt} = \frac{\partial x}{\partial t} \cdot \frac{\partial z}{\partial x} + \frac{\partial y}{\partial t} \cdot \frac{\partial z}{\partial y}$
> 
> $\hspace{6.5mm} = 1(2\sin(t)\cos(t)) * 10(x + 2y)^9 + 2(5(3t + 4)^4 * 3) * 10(x + 2y)^9$
> $\hspace{6.5mm} = 20(x + 2y)^9 (\sin(t)\cos(t) + 15(3t + 4)^4)$

> [!example]
> Find $\frac{\partial w}{\partial s}$ and $\frac{\partial w}{\partial t}$ if $w = \frac{x - z}{y + z}$, $x = s + t$, $y = st$, $z = s - t$.
> 
> (will only do $\frac{\partial w}{\partial s}$)
> 
> $\frac{\partial w}{\partial s} = \frac{\partial x}{\partial s} \cdot \frac{\partial w}{\partial x} + \frac{\partial y}{\partial s} \cdot \frac{\partial w}{\partial y} + \frac{\partial z}{\partial s} \cdot \frac{\partial w}{partial z}$
> 
> $\frac{\partial x}{\partial s} = 1$
> $\frac{\partial y}{\partial s} = t$
> $\frac{\partial z}{\partial s} = 1$
> 
> $w_x = \frac{1}{y + z}$
> $w_y = \frac{-x + z}{(y + z)^2}$
> $w_z = \frac{-x - y}{(y + z)^2}$
> 
> After substituting the above partial derivatives into the $\frac{\partial w}{\partial s}$ equation:
> $\frac{\partial w}{\partial s} = \frac{(z - x)(1 + t)}{(y + z)^2}$

> [!tip] Implicit Differentiation
> Let $F$ be differentiable on its domain and suppose $F(x, y) = k$ defines $y$ as a differentiable function of $x$. Provided $F_y \neq 0$,
> 
> $$\frac{dy}{dx} = -\frac{F_x}{F_y}$$

> [!example]
> Find $\frac{dy}{dx}$ if $x^3 + 3xy^2 - y^5 = 0$.
> 
> $F = x^3 + 3xy^2 - y^5$
> $k = 0$
> 
> $\frac{dy}{dx} = -\frac{F_x}{F_y} = \frac{-(3x^2 + 3y2)}{6xy - 5y^4}$

> [!info] Implicit Differentiation (3 variables)
> For $F(x, y, z) = k$, $\frac{\partial z}{\partial x} = -\frac{F_x}{F_z}$ and $\frac{\partial z}{\partial y} = -\frac{F_y}{F_z}$.

> [!example]
> Find $\frac{\partial z}{\partial x}$ and $\frac{\partial z}{\partial y}$ for $xy + xz + yz = 3$.
> 
> $F(x, y, z) = xy + xz + yz$
> 
> $\frac{\partial z}{\partial x} = -\frac{F_x}{F_z} = -\frac{y + z}{x + y}$
> $\frac{\partial z}{\partial y} = -\frac{F_y}{F_z} = -\frac{x + z}{x + y}$