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
> Need to find the antiderivative of $ex^2 + 4xy + 2$ with respect to $x$, and then find the antiderivative of $2x^2 - 5$ with respect to $y$.
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
> Suppose $C$ is $\vec{r}(t) = \langle x(t), y(t), z(t) \rangle$ for $a \leq t \leq b$, and $C$ lies in a region where $\vec{F} = \nabla \varphi(x, y, z) = \langle \varphi_x, \varphi_y, \varphi_z$.
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
