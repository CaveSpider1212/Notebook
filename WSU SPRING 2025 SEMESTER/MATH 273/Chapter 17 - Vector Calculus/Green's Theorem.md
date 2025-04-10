---
tags: MATH_273
created: 2025-4-10
description: Lesson 17.4
---

> [!info] 2D Curl of a Field
> The curl of a 2D field, $\text{curl}(\vec{F})$, measures the tendency of the field $\vec{F}$ to rotate counterclockwise at any given point:
> 
> $$\text{curl} (\vec{F}) = \text{curl} (\langle P, Q \rangle) = \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} = Q_x - P_y$$
> 
> Note: A field is conservative if $P_y = Q_x$, or $P_y - Q_x = 0$, meaning $\text{curl}(\vec{F}) = 0$ and $\vec{F}$ is "irrotational."

> [!info] 2D Divergence of a Field
> The divergence of a 2D field, $\text{div} (\vec{F})$ measures the tendency of the field $\vec{F}$ to "expand" or "diverge" at any given point:
> 
> $$\text{div} (\vec{F}) = \text{div} (\langle P, Q \rangle) = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} = P_x + Q_y$$
> 
> Note: $\text{div} \vec{F} = 0$ throughout $R$ means $F$ is "incompressible" on $R$.

> [!tip] Green's Theorem -- Circulation Form
> Let $C$ be a simple closed piecewise-smooth curve, oriented counterclockwise, that encloses a connected and simply connected region $R$ in the plane. Assume $F = \langle P, Q \rangle$, where $P$ and $Q$ have continuous first partial derivatives in $R$. Then
> 
> $$\displaystyle \oint_C F \cdot dr = \oint_C P dx + Q dy = \iint_R \left(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}\right) dA = \iint_R \text{curl}(\vec{F}) dA$$
> 
> The $\oint$ means circulation, and is equal to the double integral with the partial derivatives shown on the right.

> [!example]
> $F = \langle 2y, -2x \rangle$; $R$ is the region bounded by $y = \sin x$ and $y = 0$, for $0 \leq x \leq \pi$.
> 
> a) Compute the 2D curl of the vector field
> $\text{curl} (\vec{F}) = Q_x - P_y = -2 - 2 = -4$
> 
> b) Evaluate both integrals in Green's Theorem and check for consistency.
> $\oint_C F \cdot \vec{T} ds = \iint_R \text{curl} (\vec{F}) dA$
> 
> ![[4.10.25 Green's Theorem Example.png]]
> 
> RHS: $\iint_R \text{curl} (\vec{F}) dA = \int_0^{\pi} \int_0^{\sin x} (-4) dy dx = \int_0^{\pi} (-4 \sin x) dx = -4 -4 = -8$