---
tags: MATH_273
created: 2025-3-20
description: Lesson 16.5
---

Cylindrical coordinates: $(r, \theta, z)$

![[3.20.25 Cylindrical Coordinates.png]]

$dV = dz \cdot r dr d\theta = dz \cdot dA$

> [!example]
> Sketch the following sets ($r, \theta, z$ are cylindrical coordinates)
> 1. ${(r, \theta, z): 0 \leq r \leq 3, 0 \leq \theta \leq \frac{\pi}{3}, 1 \leq z \leq 4}$
> 
> ![[3.20.25 Cylindrical Set 1.png]]
> 
> 2. ${(r, \theta, z): 2r \leq z \leq 4}$
> 
> ![[3.20.25 Cylindrical Set 2 2D Graph.png]]
> Sketch:
> ![[3.20.25 Cylindrical Set 2.png]]

> [!example]
> Evaluate the following integrals using cylindrical coordinates
> 1. $\int_{-3}^3 \int_0^{\sqrt{9 - x^2}} \int_0^2 \frac{1}{1+x^2+y^2} dz dy dx$
> 
> $y = \sqrt{9 - x^2} \rightarrow x^2 + y^2 = 9$
> 
> Graph:
> ![[3.20.25 Graph 1.png]]
> 
> $= \iint_{\text{base}} \int_{\text{bottom}}^{\text{top}} \frac{1}{1 + x^2 + y^2} dz dA = \int_0^{\pi} \int_0^3 \int_0^2 \frac{1}{1 + r^2} dz r dr d\theta = \int_0^{\pi} d\theta \cdot \int_0^3 \frac{r}{1 + r^2} dr \cdot \int_0^2 dz = \pi\ln(10)$
> 
> 2. $\int_0^4 \int_0^{\frac{\sqrt{2}}{2}} \int_x^{\sqrt{1 - x^2}} e^{-x^2 - y^2} dy dx dz$
> 
> $y = \sqrt{1 - x^2} \rightarrow x^2 + y^2 = 1$
> 
> Graph:
> ![[3.20.25 Graph 2.png]]
> 
> $= \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} \int_0^1 \int_0^4 e^{-r^2} \cdot rdzdrd\theta = \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} d\theta \cdot \int_0^4 dz \cdot \int_0^1 r e^{-r^2} dr = \pi(\frac{1}{2} - \frac{1}{2}e^{-1})$