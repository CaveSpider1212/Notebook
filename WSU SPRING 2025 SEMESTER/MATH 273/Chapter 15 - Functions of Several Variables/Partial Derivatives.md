---
tags: MATH_273
created: 2025-2-6
description: Lesson 15.3
---

For $f(x, y)$, the partial derivative of $f$ with respect to $x$, denoted $\frac{df}{dx}$, represents the instantaneous rate of change of $f(x, y)$ with respect to x <u>while holding y fixed</u>.

$$\displaystyle \frac{\partial f}{\partial x} = \lim_{h \rightarrow 0} \frac{f(x + h, y) - f(x, y)}{h}$$

> [!info]
> $\frac{\partial f}{\partial x}$ is found by applying known derivative rules to the $f(x, y)$ expression while treating the character $y$ as if it represents a constant.
> 
> To find $\frac{\partial f}{\partial y}$, treat $y$ as the variable and $x$ as the constant.
> 
> Note: If the constant variable is being multiplied with the changed variable, the constant is still treated as a constant when you find the derivative, but if it is being added to the changed variable, the derivative is 0

> [!example]
> Partial derivatives of $f(x, y) = x^2 + 2xy + y^3$
> 
> $\frac{\partial f}{\partial x} = \frac{d}{dx}(x^2 + 2xy + y^3) = \frac{d}{dx}(x^2) + \frac{d}{dx}(2xy) + \frac{d}{dx}(y^3) = 3x + 2 * 1 * y + 0 = 2x + 2y$
> 
> $\frac{\partial f}{\partial y} = \frac{d}{dy}(x^2 + 2xy + y^3) = 0 + 2x * 1 + 3y^2 = 2x + 3y^2$

Graphically:
![[2.6.25 Partial Derivative Graph.png]]

> [!info] Notation: partial derivatives at arbitrary/variable $(x, y)$
> $\frac{\partial f}{\partial x}(x, y) = \frac{\partial f}{\partial x} = f_x = f_x(x, y)$
> 
> $\frac{\partial f}{\partial y}(x, y) = \frac{\partial f}{\partial y} = f_y = f_y(x, y)$
> 
> $\frac{df}{dx}$: $d$ indicates "ordinary derivative", meaning $f$ has only one input, $x$
> $\frac{\partial f}{\partial x}$: $\partial$ indicates "partial derivative", $f$ has inputs other than $x$

> [!example]
> Find the partial derivatives for $f(x, y) = 4x^3y^2 + 3x^2y^3 + 10$
> 
> $\frac{\partial f}{\partial x} = f_x = 4 * 3x^2 * y^2 + 3 * 2x * y^3 + 0 = 12x^2y^2 + 6xy^3$
> 
> $\frac{\partial f}{\partial y} = f_y = 4 * x^3 * 2y + 3 * x^2 * 3y^2 + 0 = 8x^3y + 9x^2y^2$

> [!example]
> Find the partial derivatives for $f(x, y) = e^{x^2y}$.
> 
> $f_x = e^{x^2y} * \frac{\partial}{\partial x}(x^2 y) = e^{x^2y} * 2xy$
> $f_y = e^{x^2y} * \frac{\partial}{\partial y}(x^2y) = e^{x^2y} * x^2$

> [!example]
> Find the partial derivatives for $g(x, z) = x\ln({x^2 + z^2})$.
> 
> $g_x = x * \frac{1}{x^2 + z^2} * 2x + \ln({x^2 + z^2}) * 1$
> 
> $g _z = x * \frac{1}{x^2 + z^2} * 2z = \frac{2xz}{x^2 + z^2}$

> [!example]
> Find all four second-order partial derivatives for $f(x, y) = 2x^5y^2 + x^2y$
> 
> $f_x = 10x^4y^2 + 2xy$, $f_y = 4x^5y + x^2$
> 
> $(f_x)_x = f_{xx} = 40x^3y^2 + 2y$
> $(f_x)_y = f_{xy} = 20x^4y + 2x$
> $(f_y)_x = f_{yx} = 20x^4y + 2x$
> $(f_y)_y = f_{yy} = 4x^5$

> [!tip] (Clairaut) Equality of Mixed Partial Derivatives
> $f_{xy} = f_{yx}$

> [!example]
> Find all first partial derivatives for $h(w, x, y, z) = \frac{wz}{xy}$
> 
> $h_w = \frac{z}{xy}$
> $h_x = \frac{-wz}{x^2y}$
> $h_y = \frac{-wz}{y^2x}$
> $h_z = \frac{w}{xy}$