---
tags: MATH_273
created: 2025-2-25
description: Lesson 15.7
---

> [!info] Local Maximum/Minimum Values
> Suppose $(a, b)$ is a point in region $R$ on which $f$ is defined. If $f(x, y) \leq f(a, b)$ for all $(x, y)$ in the domain of $f$ and in some open disk centered at $(a, b)$, then $f(a, b)$ is a **local maximum value** of $f$.
> 
> If $f(x, y) \geq f(a, b)$ for all $(x, y)$ in the domain of $f$ and in some open disk centered at $(a, b)$, then $f(a, b)$ is a **local minimum value** of $f$.

> [!info] Critical Point
> $(a, b)$ is a critical point of $f$ if $(a, b)$ is in the interior of the domain of $f$, and each of $f_x(a, b)$ and $f_y(a, b)$ is either 0 or undefined

> [!tip] Derivatives and Local Maximum/Minimum Values
> If $f$ has a local maximum or minimum value at $(a, b)$ and the partial derivatives $f_x$ and $f_y$ exist at $(a, b)$, then $f_x(a, b) = f_y(a, b) = 0$.

> [!info] Saddle Point
> Consider a function $f$ that is differentiable at critical point $(a, b)$. Then $f$ has a **saddle point** at $(a, b)$ if, in every open disk centered at $(a, b)$, there are points $(x, y)$ for which $f(x, y) > f(a, b)$ and points for which $f(x, y) < f(a, b)$.

> [!example]
> Find all critical points for $f(x, y) = \frac{x^3}{3} - \frac{y^3}{3} + 3xy$.
> 
> $f_x = x^2 + 3y$ <--- equation A
> $f_y = -y^2 + 3x \rightarrow y^2 = 3x \rightarrow x = \frac{y^2}{3}$ <--- equation B
> 
> Substitute equation B into equation A:
> $(\frac{y^2}{3})^2 + 3y = 0 \rightarrow \frac{y^4}{9} + 3y = 0 \rightarrow \frac{y}{9} (y^3 + 27) = 0$
> $y = 0, y = -3$
> 
> Find x values using y-values:
> $x = \frac{0^2}{3} = 0$
> $x = \frac{(-3)^2}{3} = 3$
> 
> Critical points: $(0, 0)$ and $(3, -3)$

> [!tip] Second Derivative Test
> Suppose the second partial derivatives of $f$ are continuous throughout an open disk centered at the point $(a, b)$, where $f_x(a, b) = f_y(a, b) = 0$. Let $D(x, y) = f_{xx}(x, y) f_{yy}(x, y) - (f_{xy}(x, y))^2$.
> 
> 1. If $D(a, b) > 0$ and $f_{xx}(a, b) < 0$, then $f$ has a local maximum value at $(a, b)$.
> 2. If $D(a, b) > 0$ and $f_{xx}(a, b) > 0$, then $f$ has a local minimum value at $(a, b)$.
> 3. If $D(a, b) < 0$, then $f$ has a saddle point at $(a, b)$
> 4. If $D(a, b) = 0$, then the test is inconclusive.

About $D(x, y)$:
- $f_{xx}(a, b)$ is concavity in the x-direction
- $f_{yy}(a, b)$ is concavity in the y-direction
- $f_{xy}(a, b) = \frac{\partial}{\partial y}(f_x(a, b))$

> [!example]
> Find all critical points, and then test each one using the 2nd derivative test:
> $f(x, y) = x^4 + y^4 - 4x - 32y + 10$
> 
> $f_x = 4x^3 - 4 = 0 \rightarrow x = 1$
> $f_y = 4y^3 - 32 = 0 \rightarrow y = 2$
> 
> Only critical point is $(1, 2)$.
> 
> Test function is $D(x, y) = f_{xx}f_{yy} - f_{xy}^2 = (12x^2)(12y^2) - (0)^2$
> Test $(1, 2)$: $D(1, 2) = (12)(48) - (0)^2$ <--- positive answer
> 
> $(1, 2)$ is a local minimum.

> [!example]
> Find and classify all critical points for $f(x, y) = x^2 + xy^2 - 2x + 1$
> 
> $f_x = 2x + y^2 - 2 = 0$ <--- equation A
> $f_y = 2xy = 0$ <--- equation B
> 
> Either $x = 0$ or $y = 0$:
> Equation A - $y^2 - 2 \rightarrow y = \pm \sqrt{2}$
> Equation 2 - $2x - 2 = 0 \rightarrow x = 1$
> 
> Critical points: $(0, \sqrt{2})$, $(0, -\sqrt{2})$, $(1, 0)$
> 
> $D(x, y) = f_{xx}f_{yy} - f_{xy}^2 = (2)(2x) - (2y)^2$
> $D(1, 0) = (2)(2) - (0)^2$ <--- positive
> $D(0, \pm \sqrt{2}) = (2)(0) - (\pm 2\sqrt{2})^2$ <--- negative
> 
> $(1, 0)$ is a local minimum, while $(0, \sqrt{2})$ and $(0, -\sqrt{2})$ are saddle points.

> [!example]
> For $f(x, y) = x^2y - 3$, show that $(0, 0)$ is a critical point, and that the Second Derivative Test is inconclusive at $(0, 0)$. Determine the behavior of $f$ at $(0, 0)$ by other means.
> 
> $f_x = 2xy \hspace{10mm} f_y = x^2 \hspace{10mm} f_x(0,0) = 0 \hspace{10mm} f_y(0,0) = 0$
> 
> $D(x, y) = (2y)(0) - (2x)^2$, so $D(0, 0) = (0)(0) - (0)^2 = 0$ <--- inconclusive
> 
> If $z = x^2y - 3$, then the trace $y = x$ is $z = x^3 - 3$.
> 
> $z > -3$ for $x > 0$ and $z < -3$ for $x < 0$, so $(0, -3)$ is a saddle point.

> [!example]
> Find the point on the plane $P: x + y + z = 4$ that is closest to the point $Q(5, 4, 4)$.
> 
> Distance is: $D = \sqrt{(x - 5)^2 + (y - 4)^2 + (z - 4)^2} = \sqrt{(x - 5)^2 + (y - 4)^2 + (-x - y)^2}$ <---- $z = 4 - x - y$
> So $D^2 = (x - 5)^2 + (y - 4)^2 + (x + y)^2 = f(x, y)$
> 
> Find critical points:
> $f_x = 2(x - 5) + 2(x + y) = 0 \rightarrow 4x + 2y = 10 \rightarrow 2x + y = 5$
> $f_y = 2(y - 4) + 2(x + y) = 0 \rightarrow 2x + 4y = 8 \rightarrow x + 2y = 4$
> 
> Critical point: $(2, 1)$
> 
> $D(x, y) = f_{xx} * f_{yy} - f_{xy}^2 = (4)(4) - (2)^2$
> $D(2, 1) > 0$, so local minimum
> 
> So point on $P$ closest to $Q$ is $(x, y, z) = (2, 1, 1)$ <--- $z = 4 - 2 - 1 = 1$