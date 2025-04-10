---
tags: MATH_273
created: 2025-4-3
description: Lesson 17.2
---
Curve $C: \langle x, y, z \rangle = \vec{r}(t), a \leq t \leq b$

Length of $C$ = $\int_a^b | F'(t) | dt = \int_C ds$

Integral of $f(x, y, z)$ over $C$ = $\int_C f ds = \int_C f(x, y, z) ds = \int f(x(t), y(t), z(t)) |\bar{r}'(t) | dt$ = (average value of $f$ on $C$) x (length of $C$)

> [!example]
> Evaluate $\int_C (y - z) ds$, where $C$ is $\vec{r}(t) = \langle 3\cos t, 3\sin t, 4t \rangle$, $0 \leq t \leq 2\pi$
> 
> $\vec{r}'(t) = \langle -3\sin t, 3\cos t, 4 \rangle$
> $|\vec{r}' (t)| = \sqrt{9 \sin^2 t + 9 \cos^2 t + 16} = \sqrt{9 + 16} = 5$
> 
> So $ds = 5 dt$
> 
> $\int_C (y - z) ds = \int_0^{2\pi} (3\sin t - 4t) 5 dt = -40\pi^2$ <--- substitute the $y$ and $z$ functions from $\vec{r}(t)$ into the integral

The integral of a field over a curve measures the tendency of the field to agree with motion along the curve.

At any point on a curve, the component of the field that is tangent to the curve is $\text{scal}_{\vec{r}' (t_0)} \vec{F} = \vec{F}(P) \cdot \frac{\vec{r}'(t_0)}{|\vec{r}'(t_0)|} = \vec{F} \cdot \vec{T}$.

![[4.3.25 Integral Field Tangent.png]]

> [!info] Integral of $\vec{F}$ over $C$
> $\displaystyle \int_C \vec{F} = \int_C \vec{F} \cdot \vec{T} ds = \int_C \vec{F} \cdot \frac{\vec{r}'}{| \vec{r}' |} | \vec{r}' (t) | dt = \int_C \vec{F} \cdot \vec{r}' (t) dt = \int_C \vec{F} \cdot d\vec{r}$
> 
> Gives us (avg. value of $\vec{F} \cdot \vec{T}$ on $C$) x (length of $C$)

> [!example]
> Evaluate $\int_C \vec{F} \cdot \vec{T} ds$, where $\vec{F} = \langle y, x \rangle$ and $C$ is the line segment from $(1, 1)$ to $(5, 10)$. <--- $\langle 4, 9 \rangle$
> 
> $\vec{r}(t) = \langle 1, 1 \rangle + t\langle 4, 9 \rangle = \langle 1 + 4t, 1 + 9t \rangle$
> $\vec{r}' (t) = \langle 4, 9 \rangle$
> 
> $\int_C \vec{F} \cdot \vec{T} ds = \int_C \vec{F} \cdot \vec{r}'(t) dt = \int_0^1 \langle 1 + 9t, 1 + 4t \rangle \cdot \langle 4, 9 \rangle dt = \int_0^1 (13 + 72t) dt = 49$

> [!example]
> The work required to move an object along an oriented curve $C$ in a force field $\vec{F}$ is given by $W = \int_C \vec{F} \cdot d\vec{r} = \int_C \vec{F} \cdot \vec{T} ds$. Find the work done when an object is moved through the force field $\vec{F} = \langle -y, x, z \rangle$ along the helix $\vec{r}(t) = \langle 2\cos t, 2\sin t, \frac{t}{2\pi} \rangle, 0 \leq t \leq 2\pi$.
> 
> $\int_C \vec{F} \cdot \vec{T} ds = \int_C \vec{F} \cdot \vec{r}'(t) dt$
> $= \int_C \langle -y, x, z \rangle \cdot \langle -2\sin t, 2\cos t, \frac{1}{2\pi} \rangle dt$
> $= \int_C \left(2y\sin t + 2x\cos t + \frac{1}{2\pi}z\right)dt$
> $= \int_0^{2\pi} \left(4 \sin^2 t + 4 \cos^2 t + \frac{t}{4\pi^2}\right) dt$
> $= 2\pi + \frac{1}{2}$

> [!info] Circulation
> Let $F$ be a continuous vector field on a region $D$ of $R^3$, and let $C$ be a closed smooth oriented curve in $D$. The **circulation** of $F$ on $C$ is $\int_C F \cdot T ds$, where $T$ is the unit vector tangent to $C$ consistent with the orientation.

> [!info] Flux
> Let $F = \langle f, g \rangle$ be a continuous vector field on a region $R$ of $R^2$. Let $C: r(t) = \langle x(t), y(t) \rangle$, for $a \leq t \leq b$, be a smooth oriented curve in $R$ that does not intersect itself. The **flux** of the vector field $F$ across $C$ is:
> 
> $$\displaystyle \int_C F \cdot n ds = \int_a^b (f(t) y'(t) - g(t) x'(t)) dt$$
> 
> where $n = T \times k$ is the unit normal vector and $T$ is the unit tangent vector consistent with the orientation. If $C$ is a closed curve with counterclockwise orientation, $n$ is the outward normal vector, and the flux integral gives the **outward flux** across $C$.