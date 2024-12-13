---
tags: MATH_220
description: Lesson 1.3 - Vector Equations
created: 2024-08-27
---

#### Vectors and Scalars

- **Column Vector**: matrix with only one column

$$\begin{bmatrix} x \\ y \end{bmatrix}$$

- **Scalar Multiple**: given a vector $\overrightarrow{u}$ and a scalar number $c$, the scalar multiple of $\overrightarrow{u}$ by $c$ is denoted $c\overrightarrow{u}$, and it is found by multiplying all entries of $\overrightarrow{u}$ by $c$

$$3\begin{bmatrix} 2 \\ -1 \end{bmatrix} = \begin{bmatrix} 6 \\ -3 \end{bmatrix}$$

- Adding vectors is done by adding the components in the same position (same idea as combining like terms)

#### Vectors on a Graph

- Geometric description of $\mathbb{R}^2$

![[8.27.24 R2 Graph]]

- Parallelogram rule for addition: *see [[Vectors#^60fd81]]*

- Scaling vectors: multiply everything (height and width) of the vector by the scalar
  - Unit vector is any vector of length 1

- Length of a vector: $d = \sqrt{x^2 + y^2}$

- Vectors in $\mathbb{R}^3$:

![[8.27.24 Vector R3 Diagram]]

- Now vectors in $\mathbb{R}^3$ look like $\overrightarrow{u} = \begin{bmatrix} x \\ y \\ z \end{bmatrix}$

- Vectors in $\mathbb{R}^n$
  $u = \begin{bmatrix}x_1 \\ x_2 \\ ... \\ x_n\end{bmatrix}$

#### Linear Combination

> [!info] Linear Combination
> Given vectors $v_1, v_2,....,v_p$ in $\mathbb{R}^n$ and given scalars $c_1,c_2,....,c_p$, the vector $y$ defined by
> 
> $$y = c_1v_1 + ... + c_pv_p$$
> 
> is called a linear combination of $v_1,....,v_p$ with weights $c_1,....,c_p$.

> Given that $a_1 = \begin{bmatrix}1\\-2\\0\end{bmatrix}$, $a_2 = \begin{bmatrix}2\\1\\3\end{bmatrix}$, and $b=\begin{bmatrix}8\\-1\\9\end{bmatrix}$, can $b$ be written as a linear combination of $a_1$ and $a_2$?
> 
> $b = c_1a_1 + c_2a_2$ if it is a linear combination.
> 
> $c_1\begin{bmatrix}1\\-2\\0\end{bmatrix} + c_2\begin{bmatrix}2\\1\\3\end{bmatrix} = \begin{bmatrix}8\\-1\\9\end{bmatrix}$
> 
> $\begin{bmatrix}c_1+2c_2\\-2c_1+c_2\\3c_1\end{bmatrix} = \begin{bmatrix}8\\-1\\9\end{bmatrix}$
> 
> $c_1 + 2c_2 = 8$
> $-2c_1 + c_2 = -1$
> $3c_2 = 9$
> 
> $\begin{bmatrix}1&2&|&8\\-2&1&|&-1\\0&3&|&9\end{bmatrix}$
> 
> (R1 | R2 | 1/3R3)
> $\begin{bmatrix}1&2&|&8\\-2&1&|&-1\\0&1&|&3\end{bmatrix}$
> 
> (R1-2R3 | R2-R3 | R3)
> $\begin{bmatrix}1&0&|&2\\-2&0&|&-4\\0&1&|&3\end{bmatrix}$
> 
> (R1 | R2+2R1 | R3)
> $\begin{bmatrix}1&0&|&2\\0&0&|&0\\0&1&|&3\end{bmatrix}$
> $c_1 = 2$, $c_2 = 3$
> 
> Linear combination: $b=2a_1+3a_2$

> [!info] Span
> If $v_1,....,v_p$ are in $\mathbb{R}^n$, then the set of all linear combinations of $v_1,...,v_p$ is denoted by Span{$v_1,....,v_p$} and is called the subset of $\mathbb{R}^n$ spanned (or generated) by $v_1,....,v_p$. That is, Span{$v_1,....,v_p$} is the collection of all vectors that can be written in the form
> 
> $$c_1v_1 + c_2v_2 + ... + c_pv_p$$
> 
> with $c_1,....,c_p$ scalars.