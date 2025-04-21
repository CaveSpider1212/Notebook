---
tags: MATH_273
created: 2025-4-17
description: Lesson 17.6, 17.7, 17.8
---

> [!info] Evaluation of Surface Integrals of Scalar-Valued Functions on Explicitly Defined Surfaces
> Let $f$ be a continuous function on a smooth surface $S$ given by $z = g(x, y)$, for $(x, y)$ in a region $R$. The surface integral of $f$ over $S$ is
> 
> $$\iint_S f(x, y, z) dS = \iint_D f(x, y, g(x, y)) \sqrt{g_x^2 + g_y^2 + 1} dA$$
> 
> If $f(x, y, z) = 1$, the surface integral equals the area of the surface.

> [!example]
> Find the area of the surface $z = 2(x^2 + y^2)$ for $0 \leq z \leq 8$.
> 
> $g(x, y) = 2x^2 + 2y^2$
> $g_x = 4x, g_y = 4y$
> $dS = \sqrt{(4x)^2 + (4y)^2 + 1} dA$
> 
> $2(x^2 + y^2) = 8 \rightarrow x^2 + y^2 = 4$ <--- $D$ is a disk of radius 2
> 
> $\iint_D \sqrt{16x^2 + 16y^2 + 1} dA$
> $= \int_0^{2\pi} \int_0^2 \sqrt{16 r^2 + 1} r dr d\theta = \frac{\pi}{24} (65\sqrt{65} - 1)$

> [!example]
> Let $S$ be the piece of the plane $z = 8 - x - 2y$ in the first octant, and let $f(x, y, z) = e^z$. Evaluate $\iint_S f(x, y, z) dS$.
> 
> ![[4.17.25 Surface Integral Example 1.png]]
> 
> $\iint_S f ds = \iint_D e^{8 - x - 2y} \cdot \sqrt{6}dA$
> $= \int_0^4 \int_0^{8 - 2y} e^{8 - x - 2y} \cdot \sqrt{6} dx dy = ... =  \frac{\sqrt{6}}{2} (e^8 - 9)$

> [!info] Surface Integral of a Vector Field
> Suppose $F = \langle f, g, h \rangle$ is a continuous vector field on a region of $R^3$ containing a smooth oriented surface $S$. If $S$ is defined in the form $z = s(x, y)$, for $(x, y)$ in a region $R$, then
> 
> $$\iint_S F \cdot n dS = \iint_R (- f z_x - g z_y, + h) dA$$

> [!example]
> $\vec{F} = \langle e^{-y}, 2z, xy \rangle$, $S = {(x, y, z): z = \cos y, |y| \leq \pi, 0 \leq x \leq 4}$
> Find the upward flux of $\vec{F}$ through (across) $S$.
> 
> $\iint_S \vec{F} \cdot \vec{n} dS$
> $z = g(x, y) = \cos y, g_x = 0, g_y = -\sin y$
> 
> $\iint_S \vec{F} \cdot d\vec{S} = \iint_S \vec{F} \cdot \langle -g_x, -g_y, 1 \rangle dA$
> $\iint_D \langle e^{-y}, 2z, xy \rangle \cdot \langle 0, \sin y, 1 \rangle dA$
> $= \int_0^4 \int_{-\pi}^{\pi} (0 + 2\cos y \sin y + xy) dy dx = ... = 0$

> [!tip] Divergence Theorem
> Let $F$ be a vector field whose components have continuous first partial derivatives in a connected and simply connected region $D$ in $R^3$ enclosed by an oriental surface $S$. Then
> 
> $$\iint_S F \cdot n dS = \iiint_D \nabla \cdot F dV$$
> 
> where $n$ is the outward unit normal vector on $S$.
> 
> ![[4.17.25 Divergence Theorem.png]]
> (compare against [[4.17.25 Green's Theorem Flux Form.png]])

> [!tip] Stokes' Theorem
> Let $S$ be an oriented surface in $R^3$ with a piecewise-smooth closed boundary $C$ whose orientation is consistent with that of $S$. Assume $F = \langle f, g, h \rangle$ is a vector field whose components have continuous first partial derivatives on $S$. Then
> 
> $$\oint_C F \cdot dr = \iint_S (\nabla \times F) \cdot n dS$$
> 
> ![[4.17.25 Stokes' Theorem.png]]
> (compare against [[4.17.25 Green's Theorem Circulation Form.png]])

