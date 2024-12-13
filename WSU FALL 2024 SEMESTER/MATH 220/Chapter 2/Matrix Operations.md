---
tags: MATH_220
created: 2024-09-26
description: Lesson 2.1 - Matrix Operations
---

- **Matrix addition**: we use the analog of vector addition to define matrix addition (add the entries $a_{i,j}$ and $b_{i, j}$ for all $i$ and $j$)
	- Entries must match in order to do matrix addition

> [!example]
> $$\begin{bmatrix}2&3\\-1&1\\0&1\end{bmatrix} + \begin{bmatrix}-2&-1\\1&0\\2&3\end{bmatrix} = \begin{bmatrix}0&2\\0&1\\2&4\end{bmatrix}$$

- **Matrix scalar multiplication**: for a matrix $A$ and a scalar $c$, multiply each entry in $A$ by $c$

> [!example]
> $$3\begin{bmatrix}2&3\\0&-1\\-2&0\end{bmatrix} = \begin{bmatrix}6&9\\0&-3\\-6&0\end{bmatrix}$$

> [!info] Definition
> If $A$ is an $m$ x $n$ matrix, and if $B$ is an $n$ x $p$ matrix with columns $b_1,...,b_p$, then the product $AB$ is the $m$ x $p$ matrix whose columns are $Ab_1,...,AB_p$. That is,
> 
> $$AB = A\begin{bmatrix}b_1&b_2&...&b_p\end{bmatrix} = \begin{bmatrix}Ab_1&Ab_2&...&Ab_p\end{bmatrix}$$

> [!info] Row-Column Rule for Computing AB
> If the product $AB$ is defined, then the entry in row $i$ and column $j$ of $AB$ is the sum of the products of corresponding entries from row $i$ of $A$ and column $j$ of $B$. If $(AB)_{ij}$ denotes the $(i, j)$-entry in $AB$, and if $A$ is an $m$ x $n$ matrix, then
> 
> $$(AB)_{ij} = a_{i1}b_{1j} + a_{i2}b_{2j} + ... + a_{in}b_{nj}$$

> [!example]
> Let $A = \begin{bmatrix}1&2\\3&1\end{bmatrix}$ and $B = \begin{bmatrix}3&2&1\\0&-2&3\end{bmatrix}$. Find $AB$ and $BA$.
> 
> $AB = \begin{bmatrix}1&2\\3&1\end{bmatrix} \begin{bmatrix}3&2&1\\0&-2&3\end{bmatrix} = \begin{bmatrix}1(3)+2(0)&1(2)+2(-2)&1(1)+2(3)\\3(3)+1(0)&3(2)+1(-2)&3(1)+1(3)\end{bmatrix} = \begin{bmatrix}3&-2&7\\9&4&6\end{bmatrix}$
> 
> $BA$ cannot be found because the dimensions of the matrices aren't compatible to be multiplied.

- **Powers of a matrix**: If $A$ is a $n$ x $n$ matrix and if $k$ is a positive integer, then $A^k$ denotes the product of $k$ copies of $A$
	- $A^k = A...A$
	- $A$ must be a square matrix so that the matrices are actually able to multiply with each other
	- $A^0$ is the identity matrix
	- $A^0x = x$

- **Transpose of a matrix**: Given an $m$ x $n$ matrix $A$, the transpose of $A$ is the $n$ x $m$ matrix $A^T$, whose columns are forms from the corresponding rows of $A$
	- Basically, row 1 becomes column 1, column 1 becomes row 1, row 2 becomes column 2, column 2 becomes row 2, etc.

> [!tip] Theorem
> 
> Let $A$ and $B$ denote matrices whose sizes are appropriate for the following sums and products.
> - $(A^T)^T = A$
> - $(A + B)^T = A^T + B^T$
> - For any scalar $r$, $(rA)^T = rA^t$
> - $(AB)^T = B^T A^T$