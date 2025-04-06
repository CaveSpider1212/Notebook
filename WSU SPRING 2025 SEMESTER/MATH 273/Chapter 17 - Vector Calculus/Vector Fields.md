---
tags: MATH_273
created: 2025-4-3
description: Lesson 17.1
---

Examples: $\vec{F}(x, y, z) = \langle x^2 + 2yz, z - 3x, yz^3 \rangle$ or $\vec{F}(x, y, z) = \langle x, -y \rangle$

2D fields can be hand plotted

$\vec{F}(x, y) = \langle x, -y \rangle$
$\vec{F}(1, 1) = \langle 1, -1 \rangle$
$\vec{F}(2, 1) = \langle 2, -1 \rangle$

![[4.3.25 Vector Fields Graph.png]]

Note: The gradient of a function is always a field.

For $f(x, y) = x^2 - xy^2 + 2y$, $\nabla f = \langle f_x, f_y \rangle = \langle 2x - y^2, -2xy + 2 \rangle$

Here, where $\nabla (x^2 - xy^2 + 2y) = \langle 2x - y^2, -2xy + 2 \rangle$, the function $f(x, y)$ is called a potential function for the field.

![[4.3.25 Gradient Field.png]]

> [!info]
> To find the points of vector field $\vec{F}$ tangent to a curve $C$, evaluate $\nabla C \cdot \vec{F}$. The point on $F$ is tangent to $C$ at any point where the dot product is 0. If the dot product is never 0, then there are no points tangent to $C$ in $F$.
> 
> To find the points on $\vec{F}$ normal to $C$, first find a vector $\langle a, b \rangle$ at which $\nabla C \cdot \langle a, b \rangle = 0$, and then evaluate $\langle a, b \rangle \cdot \vec{F} = 0$. If the dot product of $\langle a, b \rangle$ and $\vec{F}$ is always zero, then $F$ is always orthogonal to the tangent vector of $C$, so $F$ is normal to $C$ at all points.

> [!example]
> For $\vec{F}(x, y) = \langle x, y \rangle$ and the curve $C = {(x, y): x = 1}$,
> 
> a) Determine the points on $C$ at which $\vec{F}$ is tangent to $C$.
> None <--- from the sketch
> 
> b) Determine the points on $C$ at which $\vec{F}$ is normal to $C$.
> $(1, 0)$ <--- from the sketch
> $\langle x, y \rangle \cdot \langle 0, 1 \rangle = 0 \rightarrow y = 0, x = 1$
> 
> c) Sketch $C$ and a few vectors of $\vec{F}$ on $C$.
> 
> ![[4.3.25 Example 1 Sketch.png]]

> [!example]
> Find the gradient field $\vec{F} = \nabla\varphi$ for the potential function $\varphi(x, y) = x + y$. Sketch a few level curves of $\varphi$ and a few vectors of $\vec{F}$.
> 
> $\vec{F} = \nabla\varphi = \nabla(x + y) = \langle 1, 1 \rangle$
> 
> ![[4.3.25 Example 2 Sketch.png]]

Note: Not every field is a gradient field.