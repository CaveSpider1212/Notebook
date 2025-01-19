---
tags: MATH_273
created: 2025-1-16
description: Lesson 13.6
---

### Cylinder

For us, a "surface" is the graph of any single $xyz$ equation in $R^3$. A plane is the graph of an equation of the form $ax + by + cz = d$, and is a surface.

A "cylinder" (aka "cylindrical surface") is the graph (in $R^3$) of an $xyz$ equation which is missing one (or two) of the variables, like these:

$x^2 + z^2 = 1$

![[1.16.25 Cylinder.png]]

$y + x^2 = 4$

![[1.16.25 Cylinder 2.png]]

$z = e^{-y}$

![[1.16.25 Cylinder 3.png]]

### Non-cylinder

When all three variables are involved, picturing a surface is more complicated. It can often be accomplished using "traces." A trace of a surface is a curve which is formed by intersecting the surface with a plane of the form $x = k$, $y = k$, or $z = k$:

![[1.16.25 Trace.png]]

> [!example]
> Consider the surface $x^2 + 2z^2 + y = 4$. Let's try to graph it.
> 
> Note that the trace $y = 0$ is: $x^2 + 2z^2 = 4$
> $\rightarrow \frac{x^2}{4} + \frac{z^2}{2} = 1$ <---- making it into an ellipse equation
> $\rightarrow a = 2, b = \sqrt{2}$ <---- compare with $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$, ellipse equation
> 
> ![[1.16.25 Ellipse.png]]
> 
> Note that for other y-values, we still get elliptic traces. The trace $y = k$: $x^2 + 2z^2 + k = 4$
> $\rightarrow x^2 + 2z^2 = 4 - k$
> $\rightarrow \frac{x^2}{4 - k} + \frac{z^2}{\frac{4 - k}{2}} = 1$ <---- assumed $4 - k \neq 0$
> $\rightarrow \sqrt{4 - k}, b = \sqrt{\frac{4 - k}{2}}$
> 
> If $4 - k \gt 0$, then the traces are ellipses.
> If $4 - k = 0$, then: $X^2 + 2z^2 = 0 \rightarrow x = 0, z = 0$.
> If $4 - k \lt 0$, then: $x^2 + 2z^2 =$ (negative), no solutions.
> 
> Finally, trace $x = 0$ is: $2z^2 + y = 4$
> $\rightarrow y = 4 - 2z^2$
> 
> ![[1.16.25 Parabola.png]]
> 
> The surface:
> ![[1.16.25 Example Surface.png]]