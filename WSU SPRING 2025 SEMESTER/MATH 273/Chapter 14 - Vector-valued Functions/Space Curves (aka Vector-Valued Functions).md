---
tags: MATH_273
created: 2025-1-21
description: Lesson 14.1
---

![[1.21.25 Space Curve Example.png]]

$$\langle x, y, z \rangle = \langle f(t), g(t), h(t) \rangle$$
$$\vec{r}(t) = \langle f(t), g(t), h(t) \rangle = \langle x(t), y(t), z(t) \rangle$$

A line is a space curve and a vector-valued function:

> [!example] Linear Example
> Find a vector-valued function $\vec{r}(t)$ which describes the line through $(2, 3, 7)$ and $(4, 6, 7)$.
> 
> Distance: $\langle 2, 3, -4 \rangle$
> 
> So: $\vec{r}(t) = \langle 2, 3, 7 \rangle + t\langle 2, 3, -4 \rangle = \langle 2 + 2t, 3 + 3t, 7 - 4t \rangle$

> [!example] Non-linear Example
> Graph the space curve $\vec{r}(t) = \langle \frac{t}{\pi}, 2\sin({2t}), 2\cos({2t}) \rangle$, $0 \leq t \leq 2\pi$.
> 
> $y = 2\sin({2t}) \hspace{5mm} z = 2\cos({2t})$ <--- period is $\frac{2\pi}{2} = \pi$
> $y^2 + z^2 = (2\sin({2t}))^2 + (2\cos({2t}))^2 = 4(\cos^2({2t}) + \sin^2({2t})) = 4$ <--- $\cos^2{x} + \sin^2{x} = 1$
> 
> So, for all $t$, $y^2 + z^2 = 4$
> 
> ![[1.21.25 Non-Linear Circle.png]]
> ^ when $t = 0$, $y = 0$ and $z = 2$, and then $t = \frac{\pi}{4}$, $y = 2$ and $z = 0$
> 
> As $y$ and $z$ oscillate, $x = \frac{t}{\pi}$ grows linearly, so
> ![[1.21.25 Non-Linear Example Graph.png]]

> [!info]
> A good way to graph space curves is to make a table with $t$, plus all of the parametric functions (x, y, z, etc.), with the values of all of those functions at $t$, and then use the coordinates of x, y, and z to sketch the function.

> [!example]
> Consider $\vec{r}(t) = \langle \frac{1}{\sqrt{t}}, e^{-t}, \frac{3t}{t - 2} \rangle$. Find the domain of $\vec{r}$, discuss the continuity of $\vec{r}$, and find $\lim_{t \rightarrow \infty} \vec{r}(t)$.
> 
> Need $t \geq 0$ for $\sqrt{}$, need $\sqrt{t} \neq 0$ for $\frac{1}{\sqrt{t}}$, need $t \neq 2$ for $\frac{3t}{t - 2}$
> 
> Since all components are continuous on their domains, so is $\vec{r}(t)$.
> 
> $\lim_{t \rightarrow \infty} \langle \frac{1}{\sqrt{t}}, e^{-t}, \frac{3t}{t - 2} \rangle = \langle 0, 0, 3 \rangle$ <--- compute the limit of each individually

> [!example]
> Graph $\vec{r}(t) = \langle t, t^2, 3 \rangle$.
> 
> The curve lies in the plane $z = 3$ since it is a constant.
> 
> $x = t, y = t^2$, so $y = x^2$
> ![[1.21.25 Space Curve Graph 2.png]]