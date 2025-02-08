---
tags: MATH_273
created: 2025-1-23
description: Lesson 14.2, 14.3, 14.4, 14.5
---

> [!info]
> If $\vec{r}(t) = \langle x(t), y(t), z(t) \rangle$, then $\vec{r}'(t) = \frac{d}{dt}(\vec{r}(t)) = \frac{d\vec{r}}{dt} = \lim_{h \rightarrow 0} \frac{\vec{r}(t + h) - \vec{r}(t)}{h} = ... = \langle x'(t), y'(t), z'(t) \rangle$
> 
> $\vec{r}'(t) = \lim_{h \rightarrow 0} \frac{\vec{r}(t + h) - \vec{r}(t)}{h}$ is the "tangent vector" to $\vec{r}$ at time $t$

Interpreting $\vec{r}'(t)$ geometrically:
![[1.23.25 Tangent Drawing.png]]

The unit tangent vector to $\vec{r}(t)$ (at any $t$) is:
![[1.23.25 Unit Tangent.png]]

> [!tip] Unit Vector
>$$\vec{T}(t) = \frac{\vec{r}'(t)}{\left| \vec{r}'(t) \right|}$$

### Position, Velocity, Acceleration

> [!info] Motion in Space
> If $\vec{r}(t)$ is the position (vector) for an object as a function of time $t$, then:
> - $\vec{r}'(t)$ is the velocity vector, denoted $\vec{v}(t)$
> - $\vec{r}''(t)$ is the acceleration vector, denoted $\vec{a}(t)$
> - $\left| \vec{r}'(t) \right|$ is the speed ($\left \langle x', y', z', \rangle \right| = \sqrt{(x')^2 + (y')^2 + (z')^2}$)

> [!example]
> Find velocity, speed, and acceleration for an object whose position is $\vec{r}(t) = \langle 1, t^2, e^{-t} \rangle$.
> 
> Velocity: $\vec{r}'(t) = \vec{v}(t) = \langle 0, 2t, -e^{-t} \rangle$
> Acceleration: $\vec{r}''(t) = \vec{v}'(t) = \vec{a}(t) = \langle 0, 2, e^{-t} \rangle$
> Speed: $\left| \vec{v}(t) \right| = \sqrt{(0)^2 + (2t)^2 + (-e^{-t})^2} = \sqrt{4t^2 + e^{-2t}}$

> [!example]
> Find the unit tangent vector for $\vec{r}(t) = \langle t, 2, \frac{2}{t} \rangle$, $t > 0$.
> 
> $\vec{r}'(t) = \langle 1, 0, \frac{-2}{t^2} \rangle$
> $\vec{T}(t) = \frac{\vec{r}'(t)}{\left| \vec{r}'(t) \right|} = \frac{\langle 1, 0, \frac{-2}{t^2} \rangle}{\sqrt{1 + \frac{4}{t^4}}} = \frac{\langle t^2, 0, -2 \rangle}{\sqrt{t^4 + 4}}$

> [!example]
> Given that (for some object) $\vec{a}(t) = \langle t, e^{-t}, 1 \rangle$, $\vec{v}(0) = \langle 0, 0, 1 \rangle$, $\vec{r}(0) = \langle 4, 0, 0 \rangle$, find $\vec{r}(t)$.
> 
> $\vec{v}(t) = \int \vec{a}(t) \text{d}t = \int \langle t, e^{-t}, 1 \rangle \text{d}t = \langle \frac{1}{2}t^2 + C, -e^{-t} + D, t + E \rangle$
> 
> Now, $\vec{v}(0) = \langle 0, 0, 1 \rangle \rightarrow \langle C, -1 + D, E \rangle \rightarrow C = 0, D = 1, E = 1$
> 
> So $\vec{v}(t) = \langle \frac{1}{2}t^2, -e^{-t} + 1, t + 1 \rangle$
> 
> Next, $\vec{r}(t) = \int \langle \frac{1}{2}t^2, -e^{-t} + 1, t + 1 \rangle \text{d}t = \langle \frac{t^3}{6} + \hat{C}, e^{-t} + t + \hat{D}, \frac{t^2}{2} + t + \hat{E} \rangle$
> 
> Now, $\vec{r}(0) = \langle 4, 0, 0 \rangle \rightarrow \langle \hat{C}, 1 + \hat{D}, \hat{E} \rangle \rightarrow \hat{C} = 4, D = -1, E = 0$
> 
> So $\vec{r}(t) = \langle \frac{t^3}{6} + 4, e^{-t} + t - 1, \frac{t^2}{2} + t \rangle$

Note: you can also put the antiderivatives and constants in separate vectors instead of combining them in one vector

> [!info] Acceleration Vector
> ![[1.23.25 Acceleration Vector.png]]
> 
> $a_T = \left| \vec{a}(t) \right| \cos\theta = \frac{\left| \vec{a} \right| \left| \vec{v} \right| \cos\theta}{\left| \vec{v} \right|} = \frac{\vec{a} \cdot \vec{v}}{\left| \vec{v} \right|} = \text{scal}_{\vec{v}} \vec{a}$
> 
> $a_N = \left| \vec{a}(t) \right| \sin\theta = \frac{\left| \vec{a} \right| \left| \vec{v} \right| \sin\theta}{\left| \vec{v} \right|} = \frac{\left| \vec{a} \times \vec{v} \right|}{\left| \vec{v} \right|}$
> 
> Note: $a_T^2 + a_N^2 = \left| \vec{a}(t) \right| ^2$ for all $t$

> [!example]
> Find the tangential and normal components of acceleration, $a_T$ and $a_N$, for $\vec{r}(t) = \langle t^3, t^2 \rangle$.
> 
> $\vec{v} = \langle 3t^2, 2t \rangle$
> $\vec{a} = \langle 6t, 2 \rangle$
> $\left| \vec{v} \right| = \sqrt{9t^4 + 4t^2}$
> 
> $\vec{a} \cdot \vec{v} = 18t^3 + 4t$
> $\vec{a} \times \vec{v} = \langle 0, 0, 6t^2 \rangle$
> 
> So, $\left| \vec{a} \times \vec{v} \right| = 6t^2$
> 
> $a_T = \frac{\vec{a} \cdot \vec{v}}{\left| \vec{v} \right|} = \frac{18t^3 + 4t}{\sqrt{9t^4 + 4t^2}}$
> $a_N = \frac{\left| \vec{a} \times \vec{v} \right|}{\left| \vec{v} \right|} = \frac{6t^2}{\sqrt{9t^4 + 4t^2}}$

### Arc Length

> [!tip] Arc Length
> ![[1.28.25 Arc Length.png]]
> 
> Total length from $t = a$ to $t = b$: $\displaystyle L = \int_a^b \left| \vec{r}' (t) \right| \text{d}t$

> [!example]
> Find the length of $\vec{r}(t) = \langle 4\cos(t), 4\sin(t), 3t \rangle$, $0 \leq t \leq 6\pi$.
> 
> $\vec{r}'(t) = \vec{v}(t) = \langle -4\sin(t), 4\cos(t), 3 \rangle$
> Speed: $\left| \vec{r}'(t) \right| = \sqrt{16\sin^2(t) + 16\cos^2(t) + 9} = \sqrt{16 + 9} = 5$
> 
> $L = \int_a^b \left| \vec{r}'(t) \right| \text{d}t = \int_0^{6\pi} 5 \text{d}t = 30\pi$

> [!info] Arc Length Function
> ![[1.28.25 Arc Length Function Graph.png]]
> 
> $$\displaystyle s(t) = \int_a^t \left| \vec{r}'(u) \right| \text{d}u$$
> 
> Note: $s(a) = 0$, and for $t < a$, $s(t) < 0$

If desired, one can re-parameterize any smooth curve as a function of arc length $A$, rather than its original parameter (which is often called $t$):
![[1.28.25 Re-parameterize.png]]

It is possible that the original parameterization of the curve, $\vec{r}(t)$, already uses a parameter ($t$) which represents arc length. That is, maybe every 1 unit increase in $t$ moves us 1 unit in length along the curve. For this to be the case, we'd have to have $\left| \vec{r}'(t) \right| = 1$ (for all relevant $t$).

> [!example]
> Determine whether the curve already uses arc length as a parameter. If not, find a description of the curve that <u>does</u> use arc length as a parameter.
> 
> $\vec{r} = \langle t^2, 2t^2, 4t^2 \rangle$, $1 \leq t \leq 4$
> 
> $\vec{r}'(t) = \langle 2t, 4t, 8t \rangle$
> Speed: $\left| \vec{r}'(t) \right| = \sqrt{4t^2 + 16t^2 + 64t^2} = \sqrt{84t^2} = 2\sqrt{21} \left| t \right| = 2\sqrt{21} t$ <---- $t \neq 1$, so $t$ does not measure arc length
> 
> $s(t) = \int_1^t \left| \vec{r}'(u) \right| \text{d}u = \int_1^t 2\sqrt{21}u \text{d}u = \sqrt{21}(t^2 - 1) \rightarrow \frac{s}{\sqrt{21}} + 1 = t^2$
> 
> So $\vec{r}(t) = \langle t^2, 2t^2, 4t^2 \rangle = \langle \frac{s}{\sqrt{21}} + 1, 2(\frac{s}{\sqrt{21}} + 1), 4\left(\frac{s}{\sqrt{21}} + 1\right)\rangle = \vec{r}(s)$
> 
> $\vec{r}(s) = \langle 1, 2, 4 \rangle + s\langle \frac{1}{\sqrt{21}}, \frac{2}{\sqrt{21}} \frac{4}{\sqrt{21}} \rangle$
> 
> $1 \leq t \leq 4 \rightarrow 0 \leq s \leq 15\sqrt{21}$ <---- got $15\sqrt{21}$ by plugging in 4 into the equation relating $s$ and $t$

### Curvature

**Curvature**: measures how tightly the curve "bends" as we move along it.

![[1.28.25 Curvature.png]]

For reference, the curvature of a circle (at any point on the circle) is $\frac{1}{r}$ ($r$: radius)
Also, the curvature of a line (at all points) is 0.

> [!info] Definition of Curvature
> For a smooth, parameterized curve, the curvature is:
> 
> $$\kappa = \frac{\left| \vec{r}' \times \vec{r}'' \right|}{\left| \vec{r}' \right|^3} = \frac{\left| \vec{v} \times \vec{a} \right|}{\left| \vec{v} \right|^3}$$

> [!example]
> Find the curvature $\kappa$ for $\vec{r}(t) = \langle 4 + t^2, t, 0 \rangle$.
> 
> $\vec{r}' = \langle 2t, 1, 0 \rangle$, $\left| \vec{r}' \right| = \sqrt{4t^2 + 1}$
> $\vec{r}'' = \langle 2, 0, 0 \rangle$
> $\vec{r}' \times \vec{r}'' = \langle 0, 0, -2 \rangle$
> $\left| \vec{r}' \times \vec{r}'' \right| = 2$
> 
> So $\kappa = \frac{\left| \vec{r}' \times \vec{r}'' \right|}{\left| \vec{r}' \right|^3} = \frac{2}{(\sqrt{4t^2 + 1})^3} = \frac{2}{(4t^2 + 1)^{\frac{3}{2}}}$

![[1.30.25 Summary of Formulas Curves in Space.png]]