---
tags: MATH_273
created: 2025-3-12
description: Lesson 16.2
---

> $\int_0^4 \int_0^{\frac{1}{2}x} f(x, y) dy dx$
> 
> $0 \leq x \leq 4$, and then for any such $x$, $0, \leq y \leq \frac{1}{2}x$:
> ![[3.12.25 General Region 1.png]]
> ![[3.12.25 General Region 2.png]]
> 
> So $R$ can also be described as:
> $0 \leq y \leq 2$, and then $2y \leq x \leq 4$, so:
> $\int_0^4 \int_0^{\frac{1}{2}x} f(x, y) dy dx = \int_0^2 \int_{2y}^4 f(x, y) dx dy$

> [!example]
> Evaluate $\iint_R y^2 dA$, where $R$ is the region bounded by $x = 1$, $y = 2x + 2$, $y = -x - 1$.
> 
> ![[3.12.25 General Region Example 1.png]]
> 
> $$\iint_R y^2 dA = \int_{-1}^1 \int_{-x - 1}^{2x + 2} y^2 dy dx$$
> 
> Inner: $\int_{-(x + 1)}^{2(x + 1)} = \frac{1}{3} y^3 |_{y = -(x + 1)}^{2(x + 1)} = 3(x + 1)^3$
> 
> Outer: $\int_{-1}^1 3(x + 1)^3 dx = \frac{3}{4} (x+1)^4 |_{-1}^1 =$ 12

> [!example]
> Evaluate $\iint_R 3xy dA$, where $R$ is the region in the first quadrant bounded by $y = 2 - x$, $y = 0$ and $x = 4 - y^2$.
> 
> ![[3.12.25 General Region Example 2.png]]
> 
> $\iint_R 3xy dA = \int_0^2 \int_{2 - y}^{4 - y^2} 3xy dx dy =$ ...

> [!example]
> Reverse the order of integration, and then evaluate: $\int_0^9 \int_{\sqrt{x}}^3 \frac{1}{y^3 + 1} dy dx$
> 
> $0 \leq x \leq 9$, and then $\sqrt{x} \leq y \leq 3$
> 
> ![[3.12.25 General Region Example 3.png]]
> 
> Redescribe: $0 \leq y \leq 3$, and then $0 \leq x \leq y^2$, so:
> $\int_0^9 \int_{\sqrt{x}}^3 \frac{1}{y^3 + 1} dy dx = \int_0^3 \int_0^{y^2} \frac{1}{y^3 + 1} dx dy$
> 
> Inner: $\int_0^{y^2} \frac{1}{y^3 + 1} dx = \frac{1}{y^3 + 1} x |_{x = 0}^{x = y^2} = \frac{y^2}{y^3 + 1}$
> 
> Outer: $\int_0^3 \frac{y^2}{y^3 + 1} dy = \frac{1}{3} \ln(y^3 + 1) |_0^3 = \frac{1}{3}\ln(28)$

> [!example]
> Find the volume of the solid in the first octant bounded by the coordinate planes and the surface $z = 1 - y - x^2$.
> 
> ![[3.12.25 General Region Volume Example.png]]
> 
> Volume: $\iint_R (1 - y - x^2) dA = \int_0^1 \int_0^{1 - x^2} (1 - y - x^2) dy dx =$ ...