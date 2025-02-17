---
tags: MATH_273
created: 2025-2-4
description: Lesson 15.2
---

### Limits

![[2.4.25 Limit.png]]

$\displaystyle \lim_{(x, y) \rightarrow (a, b)} f(x, y) = L$
$\displaystyle \lim_{(x, y) \rightarrow (c, d)} f(x, y) = M$

> [!tip] Limit Laws
> - Constant function $f(x, y) = c$: $\displaystyle \lim_{(x, y) \rightarrow (a, b)} c = c$
> - Linear function $f(x, y) = x$: $\displaystyle \lim_{(x, y) \rightarrow (a, b)} x = a$
> - Linear function $f(x, y) = y$: $\displaystyle \lim_{(x, y) \rightarrow (a, b)} y = b$

> [!example]
> Evaluate $\displaystyle \lim_{(x, y) \rightarrow (2, -1)} (xy^8 - 3x^2y^2)$.
> 
> $\lim_{(x, y) \rightarrow (2, -1)} (xy^8 - 3x^2y^2) = \lim(xy^8) - \lim(3x^2y^2)$
> $= \lim(x) \times \lim(y^8) - \lim(3x^2) \times \lim(y^2)$
> $= \lim(x) \times (\lim(y))^8 - 3(\lim(x))^2 \times (\lim(y))^2$
> $= 2 \times (-1)^8 - 3(2)^2(-1)^2 = -10$

> [!info] Limits, Direct Substitution
> If $f(x, y)$ is a polynomial function of $x$ and $y$, then $\displaystyle \lim_{(x, y) \rightarrow (a, b)} f(x, y) = f(a, b)$.

> [!example]
> Evaluate $\displaystyle \lim_{(u, v) \rightarrow (1, -1)} \frac{10uv - 2v^2}{u^2 + v^2}$.
> 
> $\frac{\lim(10uv - 2v^2)}{\lim(u^2 + v^2)} = \frac{10(1)(-1) - 2(-1)^2}{(1)^2 + (-1)^2} = \frac{-12}{2} = -6$

> [!example]
> Evaluate $\displaystyle \lim_{(x, y) \rightarrow (3, 1)} \frac{x^2 - 7xy + 12y^2}{x - 3y}$ (by direct substitution, the limit is indeterminate since it is 0/0).
> 
> $\lim(\frac{(x - 3y)(x - 4y)}{x - 3y})$
> $= \lim_{(x, y) \rightarrow (3, 1)} (x - 4y) = (3) - 4(1) = -1$

> [!info] Two-Path Test for Nonexistence of Limits
> If $f(x, y)$ approaches two different values as $(x, y)$ approaches $(a, b)$ along two different paths in the domain of $f$, then $\displaystyle \lim_{(x, y) \rightarrow (a, b)} f(x, y)$ does not exist.

> [!example]
> Prove that the following limit does not exist: $\displaystyle \lim_{(x, y) \rightarrow (0, 0)} \frac{x + 2y}{x - 2y}$
> 
> Along the x-axis, y is 0, so given limit becomes $\lim_{(x, 0) \rightarrow (0, 0)} \frac{x + 2(0)}{x - 2(0)} = \lim_{x \rightarrow 0} \frac{x}{x} = 1$.
> Along the y-axis, x is 0, so original limit becomes $\lim_{(0, y) \rightarrow (0, 0)} \frac{(0) + 2y}{(0) - 2y} = \lim_{y \rightarrow 0} \frac{2y}{-2y} = -1$.
> 
> So, by 2-path test, the original limit does not exist (DNE).

> [!example]
> Show that $\displaystyle \lim_{(x, y) \rightarrow (0, 0)} \frac{xy}{x^2 + y^2}$ DNE.
> 
> Along x-axis, get $\lim_{x \rightarrow 0} \frac{x(0)}{x^2 + (0^2)} = \lim(0) = 0$.
> Along y-axis, get $\lim_{y \rightarrow 0} \frac{(0)y}{(0)^2 + y^2} = \lim(0) = 0$.
> 
> Along y = x, get $\lim_{(x, x) \rightarrow (0, 0)} \frac{x^2}{x^2 + x^2} = \lim_{x \rightarrow 0} \frac{x^2}{2x^2} = \frac{1}{2}$.

Polar coordinates can sometimes be helpful for proving that $\displaystyle \lim_{(x, y) \rightarrow (a, b)} f(x, y)$ does exist.

> [!example]
> Find $\displaystyle \lim_{(x, y) \rightarrow (0, 0)} \frac{x^2y}{x^2 + y^2}$.
> 
> ![[2.4.25 Polar Coordinates.png]]
> 
> $\lim_{r \rightarrow 0} \frac{(r\cos\theta)^2 (r\sin\theta)}{r^2}$
> $= \lim_{r \rightarrow 0} r(\cos^2 \theta \sin\theta) = 0$

### Continuity

> [!info] Continuity
> The function $f$ is continuous at the point $(a, b)$ provided
> 1. $f$ is defined at $(a, b)$
> 2. $\displaystyle \lim_{(x, y) \rightarrow (a, b)} f(x, y)$ exists
> 3. $\displaystyle \lim_{(x, y) \rightarrow (a, b)} f(x, y) = f(a, b)$

> [!info]
> Polynomial and rational functions of $(x, y)$ are continuous at all points of their domains.

> [!example]
> At which points of $R^2$ are the following functions continuous?
> 
> $f(x, y) = x^2 + 2xy - y^3$:
> $f(x, y)$ is a polynomial, so it is continuous on its domain, which is all points of $R^2$.
> 
> $f(x, y) = \frac{x^2 + y^2}{x(y^2 - 1)}$:
> This is a polynomial over a polynomial, so it is a rational function. It is continuous on its domain, which is all points except those where $x = 0$ and $y = \pm 1$.

> [!tip] Continuity of Composite Functions
> If $u = g(x, y)$ is continuous at $(a, b)$ and $z = f(u)$ is continuous at $g(a, b)$, then the composite function $z = f(g(x, y))$ is continuous at $(a, b)$.

> [!example]
> At what points of $R^2$ is $f(x, y) = \sin{(xy)}$ continuous?
> 
> $z = \sin(u)$, $u = xy$
> $z$ is continuous on its domain (all of $R$), and $u$ is a polynomial so it is also continuous on its domain (all of $R^2$), so $z = \sin({xy})$ is continuous on its domain (all of $R^2$).

> [!example]
> At what points of $R^2$ is $g(x, y) = \ln({x - y})$ continuous?
> 
> $\ln(n)$, $n = x - y$
> $\ln(n)$ is continuous on its domain ($u > 0$), and $n$ is a polynomial so it is continuous on its domain, $R^2$, so $\ln({x - y})$ is continuous wherever it is defined ($y < x$).