---
tags: MATH_273
created: 2025-4-8
description: Lesson 17.3
---

> [!info] Conservative Field
> If $\vec{F} = \nabla \varphi$ at all points in an open region $D$ (in $R^2$ or $R^3$), then $\vec{F}$ is called a **conservative field** (or a gradient field) on $D$ (and $\varphi$ is the potential function for $\vec{F}$ on $D$).

> [!info] 2D Conservative Field
> If $\vec{F} = \langle P(x, y), Q(x, y) \rangle$, then $P_y$ must equal $Q_x$ for $\vec{F}$ to be a conservative field.

> [!example]
> Determine whether $\vec{F} = \langle 2x^3 + xy^2, 2y^3 - x^2 y \rangle$ is conservative on $R^2$.
> 
> $P_y = \frac{\partial}{\partial y} (2x^3 + xy^2) = 0 + 2xy$
> $Q_x = \frac{\partial}{\partial x} (2y^3 - x^2 y) = 0 - 2xy$
> 
> $P_y$ and $Q_x$ are not equal throughout $R^2$, so $\vec{F}$ is <u>not conservative</u> on $R^2$.

> [!example]
> Determine whether $\vec{F} = \langle e^{-x} \cos y, e^{-x} \sin y \rangle$ is conservative on $R^2$.
> 
> $P_y = e^{-x} (-\sin y)$
> $Q_x = (-e^{-x}) \sin y$
> 
> $P_y$ and $Q_x$ are equal for all $(x, y)$ in $R^2$, so $\vec{F}$ is <u>conservative</u> on $R^2$.

> [!example]
> Verify that $\vec{F} = \langle 3x^2 + 4xy + 2, 2x^2 - 5 \rangle$ is conservative on $R^2$, then find a potential function for $\vec{F}$.
> 
> $P_y = 4x, Q_x = 4x$, so $\vec{F}$ is <u>conservative</u> on $R^2$.
> 
> Finding $\varphi$:
> 
> Need to find the antiderivative of $3x^2 + 4xy + 2$ with respect to $x$, and then find the antiderivative of $2x^2 - 5$ with respect to $y$.
> 
> $\varphi(x, y) = (x^2 + 2x^2 y + 2x) + (-5y)$

> [!info] 3D Conservative Field
> If $\vec{F}$ is a 3D field, say $\vec{F} = \langle P(x, y, z), Q(x, y, z), R(x, y, z)$, then the following must be true for $\vec{F}$ to be a conservative field:
> 1. $P_y = Q_x$
> 2. $P_z = R_x$
> 3. $Q_z = R_y$

> [!example]
> Determine whether $\vec{F} = \langle y + z, x + z, x + y \rangle$ is conservative on $R^3$. If it is, find a potential function.
> 
> $P_y = 1, Q_x = 1$ <--- equal
> $P_z = 1, R_x = 1$ <--- equal
> $P_z = 1, R_y = 1$ <--- equal
> 
> $\vec{F}$ is <u>conservative</u> on $R^3$.
> 
> Partial function: $\varphi(x, y, z) = yx + zx + zy$

> The Fundamental Theorem of Calc for Line Integrals:
> 
> Suppose $C$ is $\vec{r}(t) = \langle x(t), y(t), z(t) \rangle$ for $a \leq t \leq b$, and $C$ lies in a region where $\vec{F} = \nabla \varphi(x, y, z) = \langle \varphi_x, \varphi_y, \varphi_z \rangle$.
> 
> ![[4.8.25 Fundamental Theorem.png]]
> 
> Then: $\int_C \vec{F} \cdot \vec{T} ds = \int_C \vec{F} \cdot \vec{r}'(t) dt$
> $= \int_C \langle \varphi_x, \varphi_y, \varphi_z \rangle \cdot \langle x'(t), y'(t), z'(t) \rangle dt$
> $= \int_C \left(\frac{\partial \varphi}{\partial dx} \cdot \frac{dx}{dt} + \frac{\partial \varphi}{\partial y} \cdot \frac{dy}{dt} + \frac{\partial \varphi}{\partial z} \cdot \frac{dz}{dt}\right)dt$
> $= \int_a^b \frac{d}{dt} (\varphi(x(t), y(t), z(t))) dt$
> $= \varphi(x(t), y(t), z(t)) |_{t = a}^{t = b}$
> $= \varphi(\vec{r}(b)) - \varphi(\vec{r}(a))$
> $= \varphi(B) - \varphi(A)$

> [!info] Fundamental Theorem for Line Integrals
> Let $R$ be a region in $R^2$ or $R^3$ and let $\varphi$ be a differentiable potential function defined on $R$. If $F = \nabla \varphi$ (which means $F$ is conservative), then
> 
> $$\displaystyle \int_C F \cdot T ds = \int_C F \cdot dr = \varphi(B) - \varphi(A)$$
> 
> for all points $A$ and $B$ in $R$ and all piecewise-smooth oriented curves $C$ in $R$ from $A$ to $B$.

> [!example]
> Evaluate $\int_C (x^3 dx + y^3 dy)$, where $C$ is $\vec{r}(t) = \langle 1 + \sin t, \cos^2 t \rangle$, for $0 \leq t \leq \frac{\pi}{2}$.
> 
> <u>Option 1</u>
> Note that $\vec{F} = \nabla(\frac{1}{4}x^4 + \frac{1}{4}y^4)$, so:
> $\int_C \vec{F} \cdot \vec{T} ds = \varphi\left(\vec{r}\left(\frac{\pi}{2}\right)\right) - \varphi(\vec{r}(0))$
> 
> $\vec{r}\left(\frac{\pi}{2}\right) = \langle 2, 0 \rangle$
> $\vec{r}(0) = \langle 1, 1 \rangle$
> 
> $\varphi(2, 0) - \varphi(1, 1)$
> 
> $\left(\frac{1}{4}x^4 + \frac{1}{4}y^4\right) |_{(1, 1)}^{(2, 0)} = \frac{7}{2}$
> 
> <u>Option 2</u>
> $\int_C \vec{F} \cdot \vec{r}'(t) dt = \int \langle x^3, y^3 \rangle \cdot \langle \cos t, -2 \sin t \cos t \rangle dt$
> $= \int_0^{\frac{\pi}{2}} \langle (1 + \sin t)^3, (\cos^2 t)^3 \rangle \cdot \langle \cos t, -2 \sin t \cos t \rangle = ... = \frac{7}{2}$
> 
> <u>Option 3</u>
> $\int_C (x^3 dx + y^3 dy)$
> $= \int_1^2 x^3 dx + \int_1^0 y^3 dy = ... = \frac{7}{2}$ <--- got limits of integration from plugging in 0 and $\frac{\pi}{2}$ into $r(t)$

> [!example]
> Evaluate $\int_C \vec{F} \cdot d\vec{r}$, where $\vec{F} = \langle x, y^2 \rangle$ and $C$ is the triangle with vertices (1, 0), (0, 1), and (0, -1) oriented counterclockwise.
> 
> ![[4.10.25 Fundamental Theorem Example.png]]
> 
> Note: $\vec{F} = \langle x, y^2 \rangle = \nabla(\frac{1}{2}x^2 + \frac{1}{3}y^3)$, so $\oint_C \vec{F} \cdot \vec{T} ds = \varphi(\text{end}) - \varphi(\text{start}) = 0$ <--- because the end and start points of the curve are the same

![[4.10.25 Conservative Vector Fields Summary.png]]