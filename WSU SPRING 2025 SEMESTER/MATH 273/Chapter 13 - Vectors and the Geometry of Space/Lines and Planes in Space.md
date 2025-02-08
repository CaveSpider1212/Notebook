---
tags: MATH_273
created: 2025-1-9
description: Lesson 13.5
---

### Equation of a Line in Space

The equations(s) of a line in space:

![[1.9.25 Line in Space.png]]

For $\vec{r}$ to be on the line, need $\vec{r} - \vec{r}_0 = t\vec{v}$, or $\vec{r} = \vec{r}_0 + \vec{v}t$ (this is the equation of the line)

> [!info] Equation of line $l$
> $$\vec{r} = \vec{r}_0 + t\vec{v}$$
> $$\rightarrow \langle x, y, z \rangle = \langle x_0, y_0, z_0 \rangle + t\langle a, b, c \rangle$$
> $$\rightarrow \vec{r}(t) = \langle x_0+at, y_0+bt, z_0+ct \rangle$$
> 
> $x = x_0 + at$, $y = y_0 + bt$, $z = z_0 + ct$ are the parametric equations for the line for $-\infty < t < \infty$

> [!example]
> Find both the parametric and the vector equations of the specified line:
> 
> The line through (-3, 4, 6) and (5, -1, 0)
> ![[1.14.25 Vector Equation Example.png]]
> 
> ($\langle 8, -5, -6 \rangle$ is obtained by subtracting the two points from each other, which represents the distance between them)
> 
> For $\vec{r} = \vec{r}_0 + t\vec{v}$
> $\rightarrow \langle x, y, z \rangle = \langle -3, 4, 6 \rangle + t\langle 8, -5, -6 \rangle$
> or $x = -3 + 8t$, $y = 4 + -5t$, $z = 6 + -6t$

> [!example]
> Line through (1, 2, 3) that is perpendicular to the lines $x = 3 - 2t$, $y = 5 + 8t$, $z = 7 - 4t$ and $x = -2t, y=5+t, z=7-t$.
> 
> $x=3-2t, y=5+8t, z=7-4t$ = $\langle x, y, z \rangle = \langle 3, 5, 7 \rangle + t\langle -2, 8, -4 \rangle$
> 
> $x = -2t, y=5+t, z=7-t$ through (0, 5, 7), direction $\langle -2, 1, -1 \rangle$
> 
> ![[1.14.25 Vector Equation Example 2.png]]
> 
> Find $\vec{v}$ using $\vec{v}_1 \times \vec{v}_2 = \langle -2, 8, -4 \rangle \times \langle -2, 1, -1 \rangle = \langle -4, 6, 14 \rangle$ <---- we do this because we are looking for the line perpendicular to those lines
> 
> So: $\langle x, y, z \rangle = \langle 1, 2, 3 \rangle + t\langle -4, 6, 14 \rangle$ or $x = 1-4t, y = 2+6t, z=3+14t$

Given equations for two lines in space, there are four possibilities:
- The lines are parallel and do not intersect
- The lines are parallel and do intersect (they're the same line)
- The lines are "skew" (non-parallel, non-intersecting)
- The liens are not parallel and do intersect

> [!example]
> Which of the four categories above do the lines belong? If the lines intersect at one point, find it.
> 
> $$\vec{r}(t) = \langle 1, 3, 2 \rangle + t\langle 6, -7, 1 \rangle, \hspace{5mm} \vec{R}(t) = \langle 10, 6, 14 \rangle + s\langle 3, 1, 4 \rangle$$
> 
> $\vec{r}$ and $\vec{R}$ parallel? Direction vectors:
> $\langle 6, -7, 1 \rangle$ and $\langle 3, 1, 4 \rangle$ are not scalar multiples of each other, so they are NOT parallel
> 
> $\vec{r}$ and $\vec{R}$ intersect? If so, then there must be $s$ and $t$ values such that $\vec{r}(t) = \vec{R}(s)$.
> 
> $\rightarrow \langle 1, 3, 2 \rangle + t\langle 6, -7, 1 \rangle = \langle 10, 6, 14 \rangle + s\langle 3, 1, 4\rangle$
> $\rightarrow t \langle 6, -7, 1 \rangle - s\langle 3, 1, 4\rangle = \langle 9, 3, 12\rangle$
> 
> $\rightarrow 6t - 3s = 9$, $-7t - s = 3$, $t - 4s = 12$
> 
> Since $t = 0$, $s = -3$ (from solving system of equations using first and second equations) also solves the third equation, $\vec{r}$ and $\vec{R}$ do intersect, at $\vec{r}(0) = \vec{R}(-3) = \langle 1, 3, 2 \rangle$

### Equation of a Plane in Space

Suppose we know a point $P_0$ (with position vector $\vec{r}_0$) that's on the plane, and a vector $\vec{n}$ that's perpendicular (aka normal) to the plane:

![[1.14.25 Plane in Space.png]]

> [!info] Equation of a Plane
> 
> $$(\vec{r} - \vec{r}_0) \cdot \vec{n} = 0$$
> $$\rightarrow (\langle x, y, z\rangle - \langle x_0, y_0, z_0 \rangle) \cdot \langle a, b, c \rangle = 0$$
> $$\rightarrow \langle x - x_0, y - y_0, z - z_0\rangle \cdot \langle a, b, c \rangle = 0$$
> $$\rightarrow a(x - x_0) + b(y - y_0) + c(z - z_0) = 0$$
> $$\rightarrow ax + by + cz = d = ax_0 + by_0 + cz_0$$

> [!tip] Parallel and Orthogonal Planes
> Two distinct planes are parallel if their respective normal vectors are parallel (that is, the normal vectors are scalar multiples of each other).
> 
> Two planes are orthogonal if their respective normal vectors are orthogonal (that is, the dot product of the normal vectors is zero).

> [!example]
> Find an equation of the plane passing through (2, -3, 5) that is perpendicular to the line $x = 2t, y = 1+3t, z = 5+4t$.
> 
> Direction vector: $\langle 2, 3, 4 \rangle$
> 
> $a(x - x_0) + b(y - y_0) + c(z - z_0) = 0$
> $\rightarrow 2(x - 2) + 3(y + 3) + 4(z - 5) = 0$
> or: $2x + 3y + 4z = 15$

> [!example]
> Find the points at which the given plane intersects the coordinate axes, and find the equations of the lines where the plane intersects the coordinate planes. Sketch a graph of the plane.
> 
> $$3x - 2y + z = 6$$
> 
> Intercepts: $x = 2$, $y = -3$, $z = 6$ (plugging in 0 in the other variables)
> 
> ![[1.14.25 Lines Sketch.png]]

> [!example]
> Find an equation of the line passing through point $P_0(2, 1, 3)$ that is normal to the plane $2x - 4y + 10z = 10$.
> 
> $\vec{n} = \langle 2, -4, 10 \rangle$
> 
> Line: $\langle x, y, z \rangle = \langle 2, 1, 3 \rangle + t\langle2, -4, 10 \rangle$

> [!example]
> Determine which pairs of planes are parallel, which are orthogonal, and which are identical.
> 
> $$Q: 3x - 2y + z = 12 \hspace{10mm} \vec{n} = \langle 3, -2, 1\rangle$$
> $$R: -x + \frac{2}{3}y - \frac{1}{3}z = 0 \hspace{10mm} \vec{n} = \langle -1, \frac{2}{3}, -\frac{1}{3}\rangle$$
> $$S: -x + 2y + 7z = 1 \hspace{10mm} \vec{n} = \langle -1, 2, 7 \rangle$$
> $$T: \frac{3}{2}x - y + \frac{1}{2}z = 6 \hspace{10mm} \vec{n} = \langle \frac{3}{2}, -1, \frac{1}{2} \rangle$$
> 
> Planes $Q, R, T$ are parallel since they are scalar multiples of each other.
> 
> Since $\langle -1, 2, 7 \rangle \cdot \langle 3, -2, 1 \rangle = 0$, $S$ is orthogonal to $Q, R, T$.
> 
> Since $Q$ and $T$ have equivalent equations, they are identical.

Final thought: The equation $ax + by + cz = d$ represents a plane, as long as $a, b, c$ are not all zero.