---
tags: MATH_273
created: 2025-2-20
description: Lesson 15.6
---

## Tangent Planes

The tangent plane to $F(x, y, z) = k$ (a level surface for $F$) at point $P(a, b, c)$:
![[2.20.25 Tangent Plane Drawing.png]]

> [!tip] Tangent Plane Equation for $F(x, y, z) = k$
> Let $F$ be differentiable at the point $P_0 (a, b, c)$ with $\nabla F(a, b, c) \neq 0$. The plane tangent to the surface $F(x, y, z) = 0$ at $P_0$, called the **tangent plane**, is the plane passing through $P_0$ orthogonal to $\nabla F(a, b, c)$. An equation of the tangent plane is: 
> $$F_x(P) (x - a) + F_y(P) (y - b) + F_z(P) (z - c) = 0$$

The tangent plane to $z = f(x, y)$ (level surface for $F = z - f(x, y)$) at the point $P(a, b)$:
![[2.20.25 Tangent Plane Drawing 2.png]]

> [!tip] Tangent Plane Equation for $z = f(x, y)$
> $$-f_x(a, b) (x - a) - f_y(a, b) (y - b) + (z - f(a, b)) = 0$$
> $$\rightarrow z = f(a, b) + f_x(a, b) (x - a) + f_y(a, b) (y - b)$$

> [!example]
> Find an equation for the plane tangent to $yze^{xz} - 8 = 0$ at the point $(0, 2, 4)$.
> 
> $F_x = yz * e^{xz} * z \hspace{10mm} F_x(0, 2, 4) = 32$
> $F_y = ze^{xz} \hspace{10mm} F_y(0, 2, 4) = 4$
> $F_z = (yz)(e^{xz} * x) + e^{xz}(y) \hspace{10mm} F_z(0, 2, 4) = 2$
> 
> Tangent plane equation:
> $32(x - 0) + 4(y - 2) + 2(z - 4) = 0$

> [!example]
> Find an equation for the plane tangent to $z = \tan^{-1}(xy)$ at the point $(1, 1, \frac{\pi}{4})$.
> 
> Tangent plane:
> $z = f(1, 1) + f_x(1, 1) (x - 1) + f_y(1, 1) (y - 1)$
> 
> $f(1, 1) = \frac{\pi}{4}$
> $f_x = \frac{y}{1 + (xy)^2} \hspace{10mm} f_x(1, 1) = \frac{1}{2}$
> $f_y = \frac{x}{1 + (xy)^2} \hspace{10mm} f_y(1, 1) = \frac{1}{2}$
> 
> $z = \frac{\pi}{4} + \frac{1}{2}(x - 1) + \frac{1}{2}(y - 1)$

## Linear Approximation

> [!info] Linear Approximation
> The linear approximation to $f(x, y)$ at $(a, b)$ is the tangent plane, given as a function:
> $$L(x, y) = f(a, b) + f_x(a, b) (x - a) + f_y(a, b) (y - b)$$
> 
> For $(x, y)$ near $(a, b)$: $f(x, y) \approx L(x, y)$ and $\Delta z = dz$

> [!info] The differential $dz$
> Let $f$ be differentiable at the point $(x, y)$. The change in $z = f(x, y)$ as the independent variables change from $(x, y)$ to $(x + dx, y + dy)$ is denoted $\Delta z$ and is approximated by the differential $dz$:
> 
> $$\Delta z \approx dz = f_x(x, y) dx + f_y(x, y) dy$$

> [!example]
> (a) Find the linear approximation to $f(x, y) = -x^2 + 2y^2$ at $(3, -1)$
> (b) Use part (a) to estimate $f(3.1, -1.04)$
> 
> (a) -
> $L(x, y) = f(a, b) + f_x(a, b) (x - a) + f_y(a, b) (y -b)$
> 
> $f(a, y) = -7$
> $f_x = -2x \hspace{10mm} = f_x(3, -1) = -6$
> $f_y = 4y \hspace{10mm} f_y(3, -1) = -4$
> 
> $L(x, y) = -7 -6(x - 3) -4(y + 1)$
> 
> (b) -
> $(3.1, -1.04)$ is relatively close to $(3, -1)$, so we should have $f(3.1, -1.04) \approx L(3.1, -1.04) = -7 -6(0.1) -4(-0.04) =$ -7.44

> [!example]
> Find the points at which the surface $x^2 + y^2 - z^2 - 2x + 2y + 3 = 0$ has horizontal tangent planes.
> 
> We search for points $(x, y, z)$ on the given surface where $F_x = 0$, $F_y = 0$, and the original equation is true, so where $2x - 2 = 0$, $2y + 2 = 0$, and $x^2 + y^2 - z^2 - 2x + 2y + 3 = 0$
> 
> $x = 1$
> $y = -1$
> $z = \pm 1$
> 
> So, there are 2 points where the tangent plane is horizontal: $(1, -1, 1)$ and $(1, -1, -1)$

> [!example]
> Suppose $T = xy^2 + \frac{2y}{z}$. Find the values of $\Delta T$ and $dT$ when $(x, y, z)$ goes from $(1, 3, 2)$ to $(1.2, 2.9, 2.3)$.
> 
> $\Delta T$ is the exact change in $T$, which is:
> $\Delta T = (\Delta T_f) - (\Delta T_i) = T(1.2, 2.9, 2.3) - T(1, 3, 2) = 0.613739$
> 
> $dT = T_x(1, 3, 2) * dx + T_y(1, 3, 2) * dy + T_z(1, 3, 2) * d_z$
> 
> $T_x = y^2 \hspace{10mm} T_y = 2xy + \frac{2}{z} \hspace{10mm} T_z = \frac{-2y}{z^2}$
> $dx = 0.2 \hspace{10mm} dy = -0.1 \hspace{10mm} dz = 0.3$
> 
> $dT = (3)^2(0.2) + (7)(-0.1) + (\frac{-3}{2})(0.3) = 0.65$