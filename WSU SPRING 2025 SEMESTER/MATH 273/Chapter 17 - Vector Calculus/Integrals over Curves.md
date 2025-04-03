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
> $\int_C (y - z) ds = \int_0^{2\pi} (3\sin t - 4t) 5 dt = -40\pi^2$

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