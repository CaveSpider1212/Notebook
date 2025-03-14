---
tags: MATH_273
created: 2025-3-2
description: Lesson 16.1
---

Suppose we want to find the volume of the region that lies below $z = f(x, y)$ and above the rectangle $R = {(x, y): a \leq x \leq b, c \leq y \leq d} = [a, b] \times [c, d]$.

![[3.2.25 Rectangle Volume.png]]
![[3.2.25 Z Area.png]]

Area = $A(x) = \int_c^d f(x, y) dy$, treating $x$ as constant.

So, volume = $\int_a^b A(x) dx = \int_a^b (\int_c^d f(x, y)dy)dx$

> [!example]
> Evaluate $\int_1^3 (\int_0^2 x^2y dx)dy$
> 
> Inner:
> $\int_0^2 x^2y dx = \frac{1}{3}x^3 * y ]_{x = 0}^{x = 2} = \frac{1}{3}(8) * y - \frac{1}{3}(0) * y = \frac{8}{3}y$
> 
> Outer:
> $\int_1^3 \frac{8}{3} dy = \frac{8}{3} * \frac{1}{2} y^2 ]_1^3 = \frac{4}{3}(9) - \frac{4}{3}(1) = \frac{4}{3}(8) = \frac{32}{3}$

> [!tip] (Fubini) Double Integrals over Rectangular Regions
> Let $f$ be continuous on the rectangular region $R = {(x, y): a \leq x \leq b, c \leq y \leq d}$. The double integral of $f$ over $R$ may be evaluated by either of two iterated integrals:
> 
> $$\iint_R f(x, y) dA = \int_c^d \int_a^b f(x, y) dx dy = \int_a^b \int_c^d f(x, y) dy dx$$
> 
> $f(x, y)$ is the height at $(x, y)$, $dA$ is the base area at $(x, y)$ added up over $R$

> [!info]
> Several things of note for double integrals over rectangular regions:
> 
> 1. If $f(x, y) \geq 0$ on $R = [a, b] \times [c, d]$, then the value of $\int_a^b \int_c^d f(x, y) dy dx$ gives the volume under $z = f(x, y)$ and above $R$.
> 2. If $f$ is "nice enough" on $R = [a, b] \times [c, d]$ (continuity suffices), then $\int_a^b \int_c^d f(x, y) dydx = \int_c^d \int_a^b f(x, y) dxdy$ (known as Fubini's Theorem)
> 3. $\int_a^b \int_c^d f(x, y) dy dx = \int_c^d \int_a^b f(x, y) dx dy$ can also be written as $\iint_R f(x, y) dA$ (where $R = [a, b] \times [c, d]$, $R$ is the region of integration, and $dA$, the small differential piece of area in $R$, can be written as $dy dx$ or $dx dy$)
>    ![[3.2.25 Height and Area.png]]
> 4. $\iint_R 1 dA$ (also written as $\iint_R dA$) will give a number which represents both the volume of this region and the area of $R$
> 5. If $f(x, y)$ goes negative on $R$, then $\iint_R f(x, y) dA$ = (volume above $xy$ plane) - (volume below $xy$ plane)
>    ![[3.2.25 Volume if Negative.png]]
> 6. A double integral can always be thought of like $\iint_R f(x, y) dA =$ (average value of $f$ on $R$) \* (area of $R$)

> [!info] Average Value of a Function over a Plane Region
> The **average value** of an integrable function $f$ over a region $R$ is
> 
> $$\bar{f} = \frac{1}{A_R} \iint_R f(x, y) dA$$
> 
> where $A_R$ is the area of $R$

> [!example]
> Evaluate $\iint_R (x + 2y) dA$, where $R = {(x, y): 0 \leq x \leq 3, 1 \leq y \leq 4}$.
> 
> $\int_0^3 \left(\int_1^4 (x + 2y) dy\right)dx$
> 
> Inner: $(xy + y^2) ]_{y = 1}^{y = 4} = x(4 - 1) + (16 - 1) = 3x + 15$
> Outer: $\left(\frac{3}{2}x^2 + 15x\right) ]_0^3 = \frac{3}{2}(9 - 0) + 15(3 - 0) = \frac{27}{2} + 45 = 58.5$

> [!example]
> Evaluate $\int_0^1 \int_1^4 \frac{3y}{\sqrt{x + y^2}} dx dy$
> 
> Inner: $\int_1^4 \frac{3y}{\sqrt{x + y^2}} dx$
> $= \int_1^4 3y(x + y^2)^{\frac{-1}{2}} = ey * 2(x + y^2)^{\frac{1}{2}} ]_{x = 1}^{x = 4}$
> $= \int 6y(4 + y^2)^{\frac{1}{2}} - 6y * (1 + y^2)^{\frac{1}{2}}$
> 
> Outer: $\int_0^1 \left(6y(4 + y^2)^{\frac{1}{2}} - 6y\left(1 + y^2\right)^{\frac{1}{2}}\right)dy$
> $= 10\sqrt{5} - 4\sqrt{2} - 14$

> [!example]
> Compute the average value of $f(x, y) = e^{-y}$ over the region $R = {(x, y): 0 \leq x \leq 6, 0 \leq y \leq \ln(2)}$.
> 
> $\bar{f} = \frac{\iint_{R} f(x, y) dA}{\text{region\hspace{0.5mm}area}}$
> 
> Area of region: 6 ln(2)
> 
> $$\iint_R e^{-y} dA = \int_0^6 \int_0^{\ln(2)} e^{-y} dy dx$$
> Inner: $\frac{1}{2}$
> Outer: 3
> 
> So, $\bar{f} = \frac{3}{6\ln(2)} = \frac{1}{2\ln(2)} = \frac{1}{\ln(4)}$