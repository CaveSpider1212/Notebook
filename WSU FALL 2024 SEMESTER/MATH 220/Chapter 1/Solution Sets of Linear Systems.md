---
tags: MATH_220
description: Lesson 1.5 - Solution Sets of Linear Systems
created: 2024-09-05
---

### Homogenous Systems

> [!info] Homogenous
> 
> A system of linear equations is said to be homogenous if it can be written in the form $Ax = 0$, where $A$ is an $m$ x $n$ matrix and 0 is the zero vector in $R^m$.
> 
> $$\overrightarrow{x} = \begin{bmatrix}0\\...\\0\end{bmatrix}$$
> 
> Trivial solution is $\overrightarrow{x} = \overrightarrow{0}$.

> [!example]
> Determine if the homogenous system has a nontrivial solution.
> 
> $$3x_1 + 5x_2 - 4x_3 = 0$$
> $$-3x_1 - 2x_2 + 4x_3 = 0$$
> $$6x_1 + x_2 - 8x_3 = 0$$
> 
> $\begin{bmatrix}3&5&-4&|&0\\-3&-2&4&|&0\\6&1&-8&|&0\end{bmatrix}$
> 
> (using multiple row operations to get matrix into RREF)
> $\begin{bmatrix}1&0&-4/3&|&0\\0&1&0&|&0\\0&0&0&|&0\end{bmatrix}$
> 
> $x_1 - \frac{4}{3}x_3 = 0$
> $x_2 = 0$
> $0 = 0$
> 
> Solution:
> $x = \begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix} = \begin{bmatrix}\frac{4}{3}x_3\\0\\x_3\end{bmatrix} = x_3\begin{bmatrix}\frac{4}{3}\\0\\1\end{bmatrix}$
> ($x_3$ is a scalar, and the vector it is multiplied with represents the general solution)
> 
> $x = x_3\overrightarrow{v}$ (it does have a nontrivial solution)

> [!example]
> Is the system homogenous? If so, does it have a nontrivial solution?
> 
> $$x_1 + 3x_3 - 5x_3 = 0$$
> 
> $x_1 = -3x_2 + 5x_3$
> 
> $x = \begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix} = \begin{bmatrix}-3x_2+5x_3\\x_2\\x_3\end{bmatrix} = \begin{bmatrix}-3x_2\\x_2\\0\end{bmatrix} + \begin{bmatrix}5x_3\\0\\x_3\end{bmatrix} = x_2\begin{bmatrix}-3\\1\\0\end{bmatrix} + x_3\begin{bmatrix}5\\0\\1\end{bmatrix} = x_2\overrightarrow{u} + x_3\overrightarrow{v}$
> 
> This system is homogenous with a nontrivial solution.
> 
> This also allows parametric descriptions for the solution space. Instead of $x = x_2\overrightarrow{u} + x_3\overrightarrow{v}$, we say $x=s\overrightarrow{u}+t\overrightarrow{v}$ ($s$ and $t$ are general parameters).

### Solutions of Nonhomogeneous Systems

> [!example]
> Describe all solutions of $Ax = b$, where
> 
> $$A = \begin{bmatrix}3&5&-4\\-3&-2&4\\6&1&-8\end{bmatrix}, b = \begin{bmatrix}7\\-1\\4\end{bmatrix}$$
> 
> $\begin{bmatrix}3&5&-4&|&7\\-3&-2&4&|&-1\\6&1&-8&|&-4\end{bmatrix}$
> 
> (to RREF)
> $\begin{bmatrix}1&0&-4/3&|&1\\0&1&0&|&2\\0&0&0&|&0\end{bmatrix}$
> 
> $x_1 - \frac{4}{3}x_3 = 1 \rightarrow x_1 = 1 + \frac{4}{3}x_3$
> $x_2 = 2 \rightarrow x_2 = 2$
> $0 = 0 \rightarrow 0 = 0$
> 
> $x = \begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix} = \begin{bmatrix}1+\frac{4}{3}x_3\\2\\x_3\end{bmatrix} = \begin{bmatrix}1\\2\\0\end{bmatrix} + \begin{bmatrix}\frac{4}{3}x_3\\0\\x_3\end{bmatrix} = \begin{bmatrix}1\\2\\0\end{bmatrix} + x_3\begin{bmatrix}\frac{4}{3}\\0\\1\end{bmatrix} = \overrightarrow{p} + t\overrightarrow{v}$

### Writing Solution Sets in Parametric Vector Form

> [!tip] Theorem
> 
> Suppose the equation $Ax = b$ is consistent for some given $b$, and let $p$ be a solution. Then the solution set of $Ax = b$ is the set of all vectors of the form $w = p + v_h$, where $v_h$ is any solution of the homogenous equation $Ax = 0$.

- Writing a solution set in parametric vector form
	1. Row reduce the augmented matrix to RREF
	2. Express each basic variable in terms of any free variables appearing in an equation
	3. Write a typical solution $x$ as a vector whose entries depend on the free variables, if any
	4. Decompose $x$ into a linear combination of vectors using the free variables as parameters

> [!example]
> 
> Find all nontrivial solutions of $Ax = 0$ where $A = \begin{bmatrix}1&-2&1&2\\1&-1&2&5\\0&1&1&3\end{bmatrix}$.
> 
> Step 1: Row Reduce (using multiple row reduction operations)
> $\begin{bmatrix}1&0&3&8&|&0\\0&1&1&3&|&0\\0&0&0&0&|&0\end{bmatrix}$
> 
> Step 2: Express basic variables in terms of free variables
> $x_1 + 3x_3 + 8x_4 = 0 \rightarrow x_1 = -3x_3 - 8x_4$
> $x_2 + x_3 + 3x_4 = 0 \rightarrow x_2 = -x_3 - 3x_4$
> $0 = 0 \rightarrow 0 = 0$
> 
> Step 3: Write solution in vector form
> $x = \begin{bmatrix}x_1\\x_2\\x_3\\x_4\end{bmatrix} = \begin{bmatrix}-3x_3-8x_4\\-x_3-3x_4\\x_3\\x_4\end{bmatrix} = \begin{bmatrix}-3x_3\\-x_3\\x_3\\0\end{bmatrix} + \begin{bmatrix}-8x_4\\-3x_4\\0\\x_4\end{bmatrix} = x_3\begin{bmatrix}-3\\-1\\1\\0\end{bmatrix} + x_4\begin{bmatrix}-8\\-3\\0\\1\end{bmatrix}$
> 
> Step 4: Express parametrically
> $x = s\overrightarrow{u} + t\overrightarrow{v}$