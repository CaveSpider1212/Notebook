---
tags: MATH_220
created: 2024-09-12
description: Lesson 1.8 - Introduction to Linear Transformations
---

> [!info] Transformation/Function/Mapping
> A transformation (or function or mapping) $T$ from $R^n$ to $R^m$ is a rule that assigns to each vector $x$ in $R^n$ a vector $T(x)$ in $R^m$. The set $R^n$ is called the domain of $T$, and $R^m$ is called the codomain of $T$. For $x$ in $R^n$, the vector $T(x)$ in $R^m$ is called the image of $x$ (under the action of $T$). The set of all images is called the range of $T$.

> [!info] Transformation Notation
> The notation $T$ : $R^n \rightarrow R^m$ indicates that the domain of $T$ is in $R^n$ and the codomain is $R^m$.

> [!example]
> Let $A = \begin{bmatrix}1&-3\\3&5\\-1&7\end{bmatrix}$ and define a transformation $T$ : $R^2 \rightarrow R^3$ by $T(x) = Ax$.
> 
> $\begin{bmatrix}1&-3\\3&5\\-1&7\end{bmatrix} \begin{bmatrix}x_1\\x_2\end{bmatrix} = \begin{bmatrix}x_1-3x_2\\3x_1+5x_2\\-x_1+7x_2\end{bmatrix}$
> (first matrix is $A$, second matrix is $x$ or $R^2$, and the third matrix/answer is $b$ or $R^3$)

> [!example]
> If $u = \begin{bmatrix}2\\-1\end{bmatrix}$, find the image of $u$ under the transformation $T$.
> 
> $\begin{bmatrix}1&-3\\3&5\\-1&7\end{bmatrix} \begin{bmatrix}2\\-1\end{bmatrix} = \begin{bmatrix}5\\1\\-9\end{bmatrix}$

> [!example]
> Find an $x$ in $R^2$ whose image under $T$ is $\begin{bmatrix}3\\2\\-5\end{bmatrix}$. Can we find more than one $x$?
> 
> $Ax = \begin{bmatrix}3\\2\\-5\end{bmatrix}$
> $\begin{bmatrix}1&-3\\3&5\\-1&7\end{bmatrix} \begin{bmatrix}x_1\\x_2\end{bmatrix} \begin{bmatrix}3\\2\\-5\end{bmatrix}$
> 
> $\begin{bmatrix}1&-3&|&3\\3&5&|&2\\-1&7&|&-5\end{bmatrix}$
> (using row operations)
> $\begin{bmatrix}1&0&|&3/2\\0&1&|&-1/2\\0&0&|&0\end{bmatrix}$
> $x_1 = \frac{3}{2}$
> $x_2 = \frac{-1}{2}$
> $x_3 = 0$
> 
> $x = \begin{bmatrix}3/2\\-1/2\end{bmatrix}$ is the only solution

> [!info] Useful Properties for Transformations
> If $T$ is a linear transformation, then
> 
> $$T(0) = 0$$
> 
> and
> 
> $$T(cu+dv) = cT(u) + dT(v)$$
> for all vectors $u$, $v$ in the domain of $T$ and all scalars $c$, $d$.
> 
> Superposition: $T(c_1v_1 + ... + c_pv_p) = c_1T(v_1) + ... + c_pT(v_p)$