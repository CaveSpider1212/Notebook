---
tags: MATH_220
created: 2024-09-10
description: Lesson 1.7 - Linear Independence
---

### Linear Independence and Dependence

> [!info] Linear Independence vs Linear Dependence
> An indexed set of vectors ${v_1,...p,v_p}$ is said to be linearly independent if the vector equation
> 
> $$x_1v_1 + x_2v_2 + ... + x_pv_p = 0$$
> 
> has only the trivial solution. The set ${v_1,...,v_p}$ is said to be linearly dependent if there exists weights $c_1,c_2,...,c_p$, not all zero, such that
> 
> $$c_1v_1 + c_2v_2 + ... + c_pv_p = 0$$
> 
> Note: The above equation is called a linear dependence among $v_1,...,v_p$ when the weights are not all zero.
> 
> Another way of thinking about this: a set of vectors are linearly independent if you put it in an augmented matrix and they have no free variables, and the solution to all of the variables is 0

> [!tip] Theorem
> If $A$ is an $m$ x $n$ matrix, with columns $a_1,...,a_n$, and if $b$ is in $R^m$, the matrix equation
> 
> $$Ax = b$$
> 
> has the same solution set as the vector equation
> 
> $$x_1a_1 + x_2a_2 + ... + x_na_n = b$$
> 
> which, in turn, has the same solution set as the system of linear equations whose augmented matrix is
> 
> $$\begin{bmatrix}a_1&a_2&...&a_n&b\end{bmatrix}$$
> 
> This implies that given the matrix $A = \begin{bmatrix}a_1&a_2&...&a_n\end{bmatrix}$, the matrix equation $Ax = 0$ can be written as
> 
> $$x_1a_1 + x_2a_2 + ... + x_na_n = 0$$
> 
> Therefore, each linear dependence relation among the columns of $A$ corresponds to a nontrivial solution of $Ax=0$. In other words, the columns of a matrix $A$ are linearly independent if and only if $Ax = 0$ has only the trivial solution.

> [!example]
> Determine if the columns of the matrix $A = \begin{bmatrix}0&1&4\\1&2&-1\\5&8&0\end{bmatrix}$ are linearly independent.
> 
> $\begin{bmatrix}0&1&4&|&0\\1&2&-1&|&0\\5&8&0&|&0\end{bmatrix}$
> 
> (using multiple row operations)
> $\begin{bmatrix}1&2&-1&|&0\\0&1&4&|&0\\0&0&13&|&0\end{bmatrix}$
> 
> No free variable, so the only solution is $x_1=x_2=x_3=0$.

> [!tip] Theorem: Characterization of Linearly Dependent Sets
> An indexed set $S = {v_1,...,v_p}$ of two or more vectors is linearly dependent if and only if at least one of the vectors in $S$ is a linear combination of the others. In fact, if $S$ is linearly dependent and $v_1 \neq 0$, then some $v_j$ (with $j$ > 1) is a linear combination of the preceding vectors $v_1,...,v_{j-1}$.

> [!tip] Theorem
> If a set $S = {v_1,...,v_p}$ in $R^n$ contains the zero vector, then the set is linearly dependent.

> [!tip] Theorem
> If a set contains more vectors than there are entries in each vector, then the set is linearly dependent. That is, any set ${v_1, ..., v_p}$ in $R^n$ is linearly dependent if $p$ > $n$.