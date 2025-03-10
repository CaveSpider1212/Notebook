---
tags: MATH_273
created: 2025-2-13
description: Lesson 15.5
---

> [!info] Gradient
> For $f(x, y)$, the gradient of $f$ is denoted $\text{grad}(f)$ or $\nabla f$ or $\nabla f(x, y)$ and is defined as
> 
> $$\nabla f(x, y) = \langle f_x(x, y), f_y(x, y) \rangle$$
> 
> The gradient of $f$ is a field, meaning that the dimensions of its inputs and outputs are the same. Typically, the input to a field is thought of as a location, and the output is thought of as a vector associated with that input location.

> [!example]
> Find the gradient of $g(x, y) = x^2 - 4x^2y - 8xy^2$ and evaluate the gradient at $P(-1, 2)$.
> 
> $\nabla g = \langle g_x, g_y \rangle = \langle 2x - 8xy - 8y^2, -4x^2 - 16xy \rangle$
> $\nabla g(-1, 2) = \langle -2 + 16 - 32, -4 + 32 \rangle = \langle -18, 28 \rangle$

The Directional Derivative for $f(x, y)$:
![[2.18.25 Directional Derivative.png]]

The trace above line $l$:
![[2.18.25 Trace.png]]

$\frac{dz}{dt} = \frac{\partial z}{\partial x} \cdot \frac{dx}{dt} + \frac{\partial z}{\partial y} + \frac{dy}{dt}$
$\hspace{7mm} = f_x(a, b) \cdot u_1 + f_y(a, b) \cdot u_2 = \langle f_x(a, b), f_y(a, b) \rangle \cdot \langle u_1, u_2 \rangle$
$\hspace{7mm} = \nabla f(a, b) \cdot \vec{u} = D_{\vec{u}} f(a, b) = \frac{\partial f}{\partial \vec{u}}$

> [!tip] Directional Derivative
> Let $f$ be differentiable at $(a, b)$ and let $u = \langle u_1, u_2 \rangle$ be a unit vector in the $xy$-plane. The **directional derivative** of $f$ at $(a, b)$ in the direction of $u$ is:
> 
> $$D_u f(a, b) = \langle f_x(a,b), f_y(a,b) \rangle \cdot \langle u_1, u_2 \rangle = \nabla f(a,b) \cdot \vec{u}$$

> [!example]
> Compute the directional derivative of $f$ at $P$ in the direction of $\vec{v}$.
> 
> $f(x, y) = \frac{x}{x - y} \hspace{20mm} P(4, 1) \hspace{20mm} \vec{v} = \langle -1, 2 \rangle$
> 
> $D_u f(P) = \nabla f(P) \cdot \vec{u}$ <--- $\vec{u}$ must be a unit vector
> $\vec{u} = \frac{\langle -1, 2 \rangle}{\sqrt{5}}$
> $\nabla f = \langle \frac{-y}{(x - y)^2}, \frac{x}{(x - y)^2} \rangle \hspace{20mm} \nabla f(4, 1) = \langle \frac{-1}{9}, \frac{4}{9} \rangle$
> 
> $D_u f(4, 1) = \langle \frac{-1}{9}, \frac{4}{9} \rangle \cdot \frac{\langle -1, 2 \rangle}{\sqrt{5}} = \frac{1}{\sqrt{5}}$

> [!info]
> If $D_u f(P) = \nabla f(P) \cdot \vec{u} = \left| \nabla f(P) \right| \cos\theta$
> 
> $D_u f(P)$ has its maximum positive value when $\theta = 0$, meaning that $\vec{u} = \frac{\nabla f(P)}{\left| \nabla f(P) \right|}$.
> 
> Also $D_u f(P)$ has its maximum negative value when $\theta = \pi$, meaning that $\vec{u} = \frac{-\nabla f(P)}{\left| \nabla f(P) \right|}$.

> [!tip] Directions of Change
> Let $f$ be differentiable at $(a, b)$ with $\nabla f(a, b) \neq 0$.
> 
> 1. $f$ has its maximum rate of increase at $(a, b)$ in the direction of the gradient $\nabla f(a, b)$. The rate of change in this direction is $\left| \nabla f(a, b) \right|$.
> 2. $f$ has its maximum rate of decrease at $(a, b)$ in the direction of $-\nabla f(a, b)$. The rate of change in this direction is $-\left| \nabla f(a, b) \right|$.
> 3. The directional derivative is zero in any direction orthogonal to $\nabla f(a, b)$.
> 4. $\nabla f(a, b, c)$ is orthogonal to the level surface of $f$ containing $(a, b, c)$, which has equation $f(x, y, z) = k = f(a, b, c)$.

> [!tip] The Gradient and Level Curves
> Given a function $f$ differentiable at $(a, b)$, the line tangent to the level curve of $f$ at $(a, b)$ is orthogonal to the gradient $\nabla f(a, b)$, provided $\nabla f(a, b) \neq 0$.
> 
> ![[2.18.25 Level Curves.png]]

> [!example]
> a) Find the unit vectors that give the directions of <u>steepest ascent</u> and <u>steepest descent</u> at $P$.
> b) Find a vector that points in a direction of no change in $f$ at $P$.
> 
> $$f(x, y) = 2\sin(2x - 3y) \hspace{20mm} P(0, \pi)$$
> 
> a) Steepest ascent requires $\vec{u} = \frac{\nabla f(P)}{\left| \nabla f(P) \right|}$, so:
> 
> $\nabla f = \langle 4\cos(2x-3y), -6\cos(2x-3y) \rangle$
> $\nabla f(P) = \nabla f(0, \pi) = \langle -4, 6 \rangle$
> 
> For steepest ascent, $\vec{u} = \frac{\langle -4, 6 \rangle}{\left| \langle -4, 6 \rangle \right|} = \frac{\langle -2, 3 \rangle}{\left| \langle -2, 3 \rangle \right|} = \frac{\langle -2, 3 \rangle}{\sqrt{13}}$
> 
> For steepest descent, $\vec{u} = \frac{\langle 2, -3 \rangle}{\sqrt{13}}$
> 
> b) Dot product of $\nabla f(P)$ and the vector needs to be 0
> $-4 * x + 6 * y = 0$
> 
> $\langle 6, 4 \rangle$ works

> [!example]
> $f(x, y, z) = \frac{x - z}{y - z} \hspace{20mm} P(3, 2, -1) \hspace{20mm} \langle \frac{1}{3}, \frac{2}{3}, \frac{-2}{3} \rangle$
> 
> a) Find $\nabla f$ and $\nabla f(P)$
> $\nabla f = \langle \frac{1}{y - z}, \frac{-(x - z)}{(y - z)^2}, \frac{x - y}{(y - z)^2} \rangle$
> 
> $\nabla f(3, 2, -1) = \langle \frac{1}{3}, \frac{-4}{9}, \frac{1}{9} \rangle = \frac{1}{9} \langle 3, -4, 1 \rangle$
> 
> b) Find a unit vector in the direction of maximum rate of increase in $f$ at $P$.
> $\vec{u} = \frac{\nabla f(3, 2, -1)}{\left| \nabla f(3, 2, -1) \right|} = \frac{\frac{1}{9} \langle 3, -4, 1 \rangle}{\frac{1}{9} \left| \langle 3, -4, 1 \rangle \right|} = \frac{\langle 3, -4, 1 \rangle}{\sqrt{26}}$
> 
> c) Find the rate of change of $f$ in the direction of the unit vector from (b)
> $\left| \nabla f(P) \right| = \left| \frac{1}{9} \langle 3, -4, 1 \rangle \right| = \frac{1}{9} \sqrt{26}$
> 
> d) Find the directional derivative of $f$ at $P$ in the direction of the given vector ($u$ is already a unit vector)
> $D_u f(P) = \nabla f(P) \cdot \vec{u}$
> $\hspace{17mm} = \frac{1}{9} \langle 3, -4, 1 \rangle \cdot \langle \frac{1}{3}, \frac{2}{3}, \frac{-2}{3} \rangle$
> $\hspace{17mm} = \frac{1}{9} \left(1 + \frac{-8}{3} + \frac{-2}{3}\right) = \frac{1}{9} \left(\frac{-7}{3}\right)= \frac{-7}{27}$