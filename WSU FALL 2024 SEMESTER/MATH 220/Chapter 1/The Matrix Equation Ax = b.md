---
tags: MATH_220
description: Lesson 1.4 - The Matrix Equation Ax = b
created: 2024-09-03
---

### Product of a Matrix and a Column Vector

If $A$ is an $m$ x $n$ matrix, with columns $a_1, a_2, ..., a_n$, and if $x$ is in $R^n$ then the product of $A$ and $x$, denoted as $Ax$, is the linear combination of the columns of $A$ using the corresponding entries in $x$ as weights; that is,

$$Ax = \begin{bmatrix} a_1&a_2&...&a_n \end{bmatrix} \begin{bmatrix} x_1 \\ ... \\ x_n \end{bmatrix} = x_1a_1 + x_2a_2 + ... + x_na_n$$

> [!example]
> $$\begin{bmatrix} 1&2&-1 \\ 0&4&2 \end{bmatrix} \begin{bmatrix} 2 \\ -1 \\ 1 \end{bmatrix}$$
> 
> $\begin{bmatrix} 1(2)&2(-1)&-1(1) \\ 0(2)&4(-1)&2(1)\end{bmatrix}$
> 
> $\begin{bmatrix} 2&-2&-1 \\ 0&-4&2 \end{bmatrix}$

> [!example] Non-Example
> $$\begin{bmatrix} 2&-1 \\ 0&3 \\ 1&2 \end{bmatrix} \begin{bmatrix} 2 \\ 3 \\ 4\end{bmatrix}$$
> 
> Matrix sizes don't match --> undefined

> [!info] Important
> The number of columns in the first matrix must match the number of rows in the second matrix for the matrices to be able to be multiplied with each other

- **Identity Matrix**: matrix with 1's down the main diagonal and 0's elsewhere

### Matrix Equation

An equation of the form $Ax = b$ is called a matrix equation

- We can use this to rewrite systems of equations

> [!example]
> $$3x_1 - 2x_2 + x_3 = -9$$
> $$x_1 \hspace{18mm} - 5x_3 = -1$$
> $$2x_1+2x_2+3x_3 = 4$$
> 
> $A=\begin{bmatrix}3&-2&1\\1&0&-5\\2&2&3\end{bmatrix} \hspace{3mm} x = \begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}$
> 
> $Ax = \begin{bmatrix}3x_1&-2x_2&x_3\\x_1&0&-5x_3\\2x_1&2x_2&3x_3\end{bmatrix} = \begin{bmatrix}-9\\-1\\4\end{bmatrix}$

> [!tip] Theorem
> If $A$ is an $m$ x $n$ matrix, with columns $a_1, ...., a_n$, and if $b$ is in $R^m$, the matrix equation
>
> $$Ax = b$$
> 
> has the same solution set as the vector equation
> 
> $$x_1a_1 + x_2a_2 + ... + x_na_n = b$$
> which, in turn, has the same solution set as the system of linear equations whose augmented matrix is 
> 
> $$\begin{bmatrix} a_1&a_2&...&a_n&b \end{bmatrix}$$

> Let $A = \begin{bmatrix} 1&3&4\\-2&2&-2\\-3&7&0\end{bmatrix}$ and $b=\begin{bmatrix}b_1\\b_2\\b_3\end{bmatrix}$. Is the equation $Ax=b$ consistent for all possible $b_1, b_2, b_3?$
> 
> $\begin{bmatrix}1&3&4&|&b_1\\-2&2&-2&|&b_2\\-3&7&0&|&b_3\end{bmatrix}$
> 
> (using several row reduction operations)
> $\begin{bmatrix}1&3&4&|&b_1\\0&8&6&|&b_2+2b_1\\0&0&0&|&b_3-2b_2-b_1\end{bmatrix}$
> 
> $0 = b_3-2b_2-b_1$
> Doesn't work for all $b_1, b_2,$ and $b_3$.

> [!tip] Theorem
> Let $A$ be an $m$ x $n$ matrix. Then the following statements are logically equivalent. That is, for a particular $A$, either they are all true statements or they are all false statements.
> 
> 1. For each $b$ in $R^m$, the equation $Ax = b$ has a solution.
> 2. Each $b$ in $R^m$ is a linear combination of the columns of $A$.
> 3. The columns of $A$ span $R^m$.
> 4. $A$ has a pivot position in every row (in the coefficient matrix).
> 
> If one of the 4 above are true, then they all are true. If any one of them are false, then all 4 of them are false.

^859146

> [!tip] Theorem
> 
> If $A$ is an $m$ x $n$ matrix, $u$ and $v$ are vectors in $R^n$, and $c$ is a scalar, then:
> 
> 1. $A(u+v) = Au + Av$
> 2. $A(cu) = c(Au)$