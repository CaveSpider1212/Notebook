---
tags: MATH_273
created: 2025-3-12
description: Lesson 16.3
---

![[3.12.25 Polar Coordinate.png]]

Sometimes, regions in 2D are more easily or conveniently described using polar coordinates; especially disks, annuli, or sectors of such:
![[3.12.25 Polar Coordinate Disks.png]]

> [!example]
> Evaluate $\iint_R 2xy dA$, where $R = {(r, \theta): 1 \leq r \leq 3, 0 \leq \theta \leq \frac{\pi}{2}}$.
> 
> $\iint_R 2xy dA = \int_0^{\frac{\pi}{2}} \int_1^3 2(r\cos\theta)(r\sin\theta) r\cdot dr d\theta$
> $= \int_0^{\frac{\pi}{2}} \int_1^3 2r^3 \cdot \sin\theta \cos\theta dr d\theta$
> $= \int_0^{\frac{\pi}{2}} \sin\theta \cos\theta \left(\int_1^3 2r^3 dr\right)d\theta$
> $= \int_0^{\frac{\pi}{2}} \sin\theta \cos\theta d\theta \cdot \int_1^3 2r^3 dr =$ 20

> [!example]
> Evaluate $\iint_R \frac{dA}{\sqrt{16 - x^2 - y^2}}$, where $R = {(x, y): x^2 + y^2 \leq 4, x \leq 0, y \leq 0}$.
> 
> $16 - x^2 - y^2 = 16 - (x^2 + y^2) = 16 - r^2$
> 
> ![[3.12.25 Polar Example Graph 1.png]]
> 
> $\int_0^{\frac{\pi}{2}} \left(\int_0^2 \frac{1}{\sqrt{16 - r^2}} r \cdot dr\right)d\theta$
> $\int_0^{\frac{\pi}{2}} d\theta \cdot \int_0^2 r(16 - r^2)^{\frac{-1}{2}} dr = \frac{\pi}{2} \cdot \left(-(16 - r^2)^{\frac{1}{2}}\right)|_0^2$
> $= \pi(2 - \sqrt{3})$

> [!example]
> Evaluate $\int_0^3 \int_0^{\sqrt{9 - x^2}} \sqrt{x^2 + y^2} dy dx$
> 
> ![[3.12.25 Polar Example Graph 2.png]]
> 
> $\int_0^{\frac{\pi}{2}} \left(\int_0^3 r \cdot r \cdot dr\right) d\theta = \int_0^{\frac{\pi}{2}} d\theta \cdot \int_0^3 r^2 dr = \frac{9\pi}{2}$

> [!example]
> Find the average distance between the points in the disk ${(r, \theta): 0 \leq r \leq 9}$ and the origin.
> 
> ![[3.12.25 Polar Example Graph 3.png]]
> 
> $\bar{r} = \frac{\iint_D r dA}{\text{area}} = \frac{1}{\pi a^2} \int_0^{2\pi} \int_0^a r \cdot r \cdot dr d\theta = \frac{2}{3}a$