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
> $a_N = \left| \vec{a}(t) \right| \sin\theta = \frac{\left| \vec{a} \right| \left| \vec{v} \right| \sin\theta}{\left| \vec{v} \right|} = \frac{\vec{a} \times \vec{v}}{\left| \vec{v} \right|}$
> 
> Note: $a_T^2 + a_N^2 = \left| \vec{a}(t) \right| ^2$ for all $t$