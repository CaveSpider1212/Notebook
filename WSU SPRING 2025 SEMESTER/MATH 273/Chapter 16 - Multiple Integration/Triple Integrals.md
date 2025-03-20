---
tags: MATH_273
created: 2025-3-18
description: Lesson 16.4
---

$\displaystyle \iiint_E f(x, y, z) dV$ = (average value of $f(x, y, z)$ on $E$)(volume of $E$)

$\displaystyle \iiint_E 1 dV = \iiint_E dV =$ (volume of $E$)

> [!example]
> Evaluate $\int_0^1 \int_{-1}^2 \int_1^3 (xy + 2yz) dy dz dx$
> 
> Inner: $\int_1^3 (xy + 2yz) dy$
> $\left(\frac{x}{2} y^2 + y^2 z\right)|_1^3$
> $= 4x + 8z$
> 
> Middle: $\int_{-1}^2 (4x + 8z) dz$
> $(4xz + 4z^2) |_{-1}^2$
> $= 12x + 12$
> 
> Outer: $\int_0^1 (12x + 12) dx$
> $(6x^2 + 12x) |_0^1$
> $= 18$

> [!example]
> Use a triple integral to find the volume of the solid int he first octant bounded by the plane $2x + 3y + 6z = 12$ and the coordinate planes.
> 
> ![[3.18.25 Triple Integral Example Region 1.png]]
> 
> $\iiint_E 1 dV$
> $= \iint_R \int_0^{2 - \frac{1}{3}x - \frac{1}{6}y} 1 dz dA$
> 
> ![[3.18.25 Triple Integral Example 1 2D Region.png]]
> 
> $= \int_0^6 \int_0^{4 - \frac{2}{3}x} \int_0^{2 - \frac{1}{3}x - \frac{1}{6}y} 1 dz dy dx = ...$

Note: The volume of a solid region (with bases at $z = g(x, y)$ and $z = h(x, y)$) can often be found using a triple or double integral.

(Volume of $E$) = $\iiint_E 1 dV = \iint_R \int_{g(x, y)}^{h(x, y)} 1 dz dA$

> [!example]
> Find the volume of the solid bounded by the paraboloid $z = 2 - x^2 - y^2$ and the plane $z = 1$.
> 
> Vol = $\iiint_E 1 dV$
> $= \iint_R \int_1^{2 - x^2 - y^2} 1 dz dA$
> $= \iint_R (2 - x^2 - y^2 - 1) dA$
> $= \int_0^{2\pi} \int_0^1 (1 - r^2) r dr d\theta$
> $= 2\pi\left(\frac{1}{2} - \frac{1}{4}\right)= \frac{\pi}{2}$

> [!example]
> Find the volume of the solid bounded below by cone $z = \sqrt{x^2 + y^2}$ and above by the sphere $x^2 + y^2 + z^2 = 8$.
> 
> ![[3.18.25 Triple Integral Example 2 Region.png]]
> 
> Vol = $\iint_R (\sqrt{8 - x^2 - y^2} - \sqrt{x^2 + y^2}) dA$
> $\int_0^{2\pi} \int_0^2 (\sqrt{8 - r^2} r) r dr d\theta = ...$