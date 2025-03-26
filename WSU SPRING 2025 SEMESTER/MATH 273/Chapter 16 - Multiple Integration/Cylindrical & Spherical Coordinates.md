---
tags: MATH_273
created: 2025-3-20
description: Lesson 16.5
---

### Cylindrical Coordinates

> [!info] Cylindrical Coordinates
> ![[3.20.25 Cylindrical Coordinates.png]]
> 
> $$(r, \theta, z)$$
> 
> $dV = dz \cdot r dr d\theta = dz \cdot dA$

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

> [!example]
> Find the volume of the solid bounded by the hyperboloid $z = 3 - \sqrt{1 + x^2 + y^2}$ and the plane $z = 0$.
> 
> $z = 3 - \sqrt{1 + x^2 + y^2} = 3 - \sqrt{1 + r^2} \rightarrow \sqrt{1 + r^2} = 3 - z \rightarrow 1 + r^2 = (3 - z)^2 \rightarrow (3 - z)^2 - r^2 = 1$ <--- shifted hyperbola (3 units up the z-axis)
> 
> Base boundary: $3 - \sqrt{1 + r^2} = 0 \rightarrow r = \sqrt{8}$ <--- where $z = 3 - \sqrt{1 + r^2} = 3 - \sqrt{1 + x^2 + y^2}$ intersects with the plane $z = 0$
> 
> Volume: $\int_0^{2\pi} \int_0^{\sqrt{8}} (3 - \sqrt{1 + r^2}) r dr d\theta = ...$

### Spherical Coordinates

> [!info] Spherical Coordinates
> ![[3.25.25 Spherical Coordinates.png]]
> 
> $$(\rho, \phi, \theta)$$
> 
> $r = \rho \sin\phi$
> $z = \rho \cos\phi$
> $x = r \cos\theta = \rho \sin\phi \cos\theta$
> $y = r \sin\theta = \rho \sin\phi \sin\theta$
> $\rho^2 = r^2 + z^2 = x^2 + y^2 + z^2$
> $\tan\theta = \frac{y}{x}$
> $\tan\phi = \frac{r}{z}$
> 
> $dV = dxdydx = r dr d\theta dz = \rho^2 \sin\phi d\rho d\phi d\theta$
> 
> ($\rho \geq 0$, $0 \leq \theta \leq 2\pi$, $0 \leq \phi \leq \pi$)

> [!example]
> Describe the set ${(\rho, \phi, \theta): 1 \leq \rho \leq 3}$.
> 
> All points on or between the spheres $\rho = 1$ and $\rho = 3$

> [!example]
> Describe: ${(\rho, \phi, \theta): \rho = 2\sec\phi, 0 \leq \phi \leq \frac{\pi}{2}}$.
> 
> $\rho = \frac{2}{\cos\phi} \rightarrow \rho \cos\phi = 2 \rightarrow z = 2$
> 
> This is the plane $z = 2$.

> [!example]
> Evaluate: $\int_0^{2\pi} \int_0^{\frac{\pi}{3}} \int_0^{4\sec\phi} \rho^2 \sin\phi d\rho d\phi d\theta$
> 
> Inner: $\int_0^{4\sec\phi} \rho^2 \sin\phi d\rho = \frac{1}{3} \rho^3 \sin\phi |_{\rho = 0}^{4\sec\phi} = \frac{64}{3}\sec^2 \phi \sin\phi = \frac{64}{3} \cdot \frac{\sin\phi}{\cos^3 \phi}$
> 
> Middle: $\int_0^{\frac{\pi}{3}} \frac{64}{3} \cdot \frac{\sin\phi}{(\cos\phi)^3} d\phi$
> $\frac{-64}{3} \int_1^{\frac{1}{2}} \frac{1}{u^3} du$ <--- after u-sub
> $\frac{64}{3} \left(\frac{-1}{2} u^{-2} |_{\frac{1}{2}}^{1}\right)$
> $= 32$
> 
> Outer: $\int_0^{2\pi} 32 d\theta = 32(2\pi - 0) = 64\pi$

> [!example]
> Evaluate $\iiint_D (x^2 + y^2 + z^2)^{\frac{5}{2}} dV$, where $D$ is the unit ball.
> 
> Unit ball: $0 \leq \rho \leq 1$, $0 \leq \phi \leq \pi$, $0 \leq \theta \leq 2\pi$
> 
> $\int_0^{2\pi} \int_0^{\pi} \int_0^1 \rho^5 \cdot \rho^2 \sin\phi d\rho d\phi d\theta$ <--- $x^2 + y^2 + z^2 = \rho^2$ and $dV = \rho^2 \sin\phi d\rho d\phi d\theta$
> $= \int_0^{2\pi} d\theta \cdot \int_0^{\pi} \sin\phi d\phi \cdot \int_0^1 \rho^7 d\rho$
> $= \frac{\pi}{2}$

> [!example]
> Find the volume of the solid outside of the cone $\phi = \frac{\pi}{4}$ and inside the sphere $\rho = 4\cos\phi$.
> 
> ![[3.25.25 Spherical Coordinate Example.png]]
> 
> Region: $0 \leq \theta \leq 2\pi$, $\frac{\pi}{4} \leq \phi \leq \frac{\pi}{2}$, $0 \leq \rho \leq 4\cos\phi$
> 
> Vol = $\int_0^{2\pi} \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} \int_0^{4\cos\phi} \rho^2 \sin\phi d\rho d\phi d\theta$
> $= 2\pi \cdot \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} \sin\phi \left(\int_0^{4\cos\phi} \rho^2 d\rho\right)d\phi$
> $= \frac{8\pi}{3}$