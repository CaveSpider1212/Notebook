---
tags: MATH_220
created: 2024-10-24
description: Lesson 3.3 - Cramer's Rule, Volume, and Linear Transformations
---

> [!tip] Theorem: Cramer's Rule
> Let $A$ be an invertible $n$ x $n$ matrix. For any $b$ in $R^n$, the unique solutions of $x$ of $Ax = b$ has entries given by
> 
> $$x_i = \frac{detA_i(b)}{detA}, \hspace{10mm} i = 1, 2, ..., n$$
> 
> where $A_i(b)$ is the matrix obtained from $A$ by replacing column $i$ by the vector $b$.

> [!example]
> Determine all values of $t$ such that the following system has a unique solution.
> 
> $$3tx_1 - 2x_2 = 4$$
> $$-6x_1 + tx_2 = 1$$
> 
> $A = \begin{bmatrix}3t&-2\\-6&t\end{bmatrix} \hspace{5mm} B = \begin{bmatrix}4\\1\end{bmatrix}$
> $A_1(b) = \begin{bmatrix}4&-2\\1&t\end{bmatrix} \hspace{5mm} A_2(b) = \begin{bmatrix}3t&4\\-6&1\end{bmatrix}$
> $detA = 3(t+2)(t-2) \hspace{4mm} detA_1(b) = 2(2t + 1) \hspace{4mm} detA_2(b) = 3(t + 8)$
> $x_1 = \frac{detA_1(b)}{detA} = \frac{2(2t + 1)}{3(t+2)(t-2)}$
> $x_2 = \frac{detA_2(b)}{detA} = \frac{(t + 8)}{(t + 2)(t - 2)}$
> 
> $t \neq -2$ and $t \neq 2$ implies $A$ is not invertible, implies there is not a unique solution.

Generating $A^{-1}$:
$A_x = e_j$ ($e_j$ is the $j$th column of $I$)
$x_i = \frac{detA_i(e_j)}{detA}$ 
- $i$th entry of the vector whose image is the $j$th column of the identity matrix
- Adjoining each $x$ for each $e_j$ is essentially creating the inverse

In particular ($i$th, $j$th) entry of the inverse is
$$x_i = \frac{det A_i(e_j)}{det A}$$

> [!tip] Theorem: An Inverse Formula
> Let $A$ be an invertible $n$ x $n$ matrix. Then
> $$A^{-1} = \frac{1}{det A}adj A$$
> 
> Finding adj$A$ (adjugate of $A$):
> 1. Take the cofactors of each entry in $A$ using cofactor expansion (but without using the entry as a coefficient)
> 2. Put the cofactors in a cofactor matrix
> 3. Transpose the cofactor matrix to get adj$A$ (the rows become the columns and vice versa)

> [!tip] Theorem
> If $A$ is a $2 \times 2$ matrix, the area of the parallelogram determined by the columns of $A$ is $\left|detA\right|$. If $A$ is a $3 \times 3$ matrix, the volume of the parallelepiped determined by the columns of $A$ is $\left|detA\right|$.

> [!tip] Theorem
> Let $T : R^2 \rightarrow R^2$ be the linear transformation determined by the $2 \times 2$ matrix $A$. If $S$ is a parallelogram in $R^2$, then
> 
> $${Area_{T(S)}} = \left|detA\right| \cdot {Area_{S}}$$
> 
> If $T$ is determined by a $3 \times 3$ matrix $A$, and if $S$ is a parallelepiped in $R^3$, then
> 
> $${V_{T(S)}} = \left|detA\right| \cdot {V_{(S)}}$$