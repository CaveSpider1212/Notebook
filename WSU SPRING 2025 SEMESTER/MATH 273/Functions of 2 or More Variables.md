---
tags: MATH_273
created: 2025-1-30
description: Lesson 15.1
---

> Here's one: $f(x, y) = \sqrt{25 - x^2 - y^2}$
> 
> The domain of $f$ is the set of all $(x, y)$ for which $f(x, y)$ is defined, which is:
> $25 - x^2 - y^2 \geq 0$
> $25 \geq x^2 + y^2$
> $x^2 + y^2 \leq 25$
> (pg. 4 drawing)
> 
> $D = \{ (x, y): x^2 + y^2 \leq 25 \}$
> 
> The range of $f$ is the set of all achievable output values, which (in this case) is:
> $0 \leq f(x, y) \leq 5$ or $[0, 5]$
> 
> The graph of $f$ is the graph of $z = f(x, y)$. That is, call the output $z$, then graph the resulting relation in $R^3$:
> $z = \sqrt{25 - x^2 - y^2}$
> $\rightarrow z^2 = 25 - x^2 - y^2$
> $\rightarrow x^2 + y^2 + z^2 = 25$ <---- this is a sphere, radius 5, under $\vec{O}$........this is also the top half of that sphere ($z \geq 0$) because of the domain
> (pg. 6 drawing)

> [!example]
> Find the domain of $g(x, y) = \ln({x^2 - y})$.
> 
> Domain:
> $x^2 - y > 0$
> $\rightarrow x^2 > y$
> $\rightarrow y < x^2$
> 
> (pg. 7 drawing)
> 
> $D = \{ (x, y): y < x^2 \}$
> 
> (other pg. 7 drawing)

> [!example]
> Sketch a graph of the function $f(x, y) = 6 - x - 2y$. Identify the surface by name, and state state its domain and range.
> 
> $f(x, y) = 6 - x - 2y$
> $\rightarrow z = 6 - x - 2y$
> $\rightarrow x + 2y + z = 6$ <---- this is a <u>plane</u>
> 
> Graph:
> (pg. 8 drawing)
> 
> Domain of $f$: $R^2 = R \times R = (-\infty, \infty) \times (\infty, \infty) = (\infty, \infty)^2$
> Range of $f$: $(\infty, \infty) = R$

> [!example]
> Sketch a graph of the function $h(x, y) = 2x^2 + 3y^2$. Identify the surface by name, and state state its domain and range.
> 
> Domain: $R^2$
> Range: $[0, \infty)$
> 
> $z = 2x^2 + 3y^2$
> 
> Traces:
> $z = 0$: $0 = 2x^2 + 3y^2$ <---- $x = 0$ and $y = 0$
> $z = k < 0$: (negative) = $2x^2 + 3y^2$ <---- no solutions
> $z = k > 0$: $k = 2x^2 + 3y^2 \rightarrow 1 = \frac{x^2}{\frac{K}{2}} + \frac{y^2}{\frac{k}{3}}$ <---- $a^2 = \frac{k}{2}$ and $b^2 = \frac{k}{3}$ in the ellipse formula
> 
> $y = 0$: $z = 2x^2$ <---- parabola
> 
> (pg. 10 drawing)
> 
> We can use the level curves of $h$ to form a "contour map" of $h$:
> (pg. 11 drawing)

> [!example]
> Graph several level curves of the function in the given window. Label at least two level curves with their z-values.
> 
> $z = x - y^2, [0, 4] \times [-2, 2]$
> 
> Traces:
> $z = 0$: $0 = x - y^2 \rightarrow x = y^2$
> $z = 1$: $1 = x - y^2 \rightarrow x = y^2 + 1$
> $z = k$: $k = x - y^2 \rightarrow x = y^2 + k$
> 
> (pg. 12 drawing)

> [!example]
> Find the domain. Describe it if possible: $p(x, y, z) = \sqrt{x^2 + y^2 + z^2 - 9}$
> 
> Domain: $x^2 + y^2 + z^2 - 9 \geq 0$
> $\rightarrow x^2 + y^2 + z^2 \geq 9$ <---- all points $(x, y, z)$ on or outside of the sphere $x^2 + y^2 + z^2 = 9$