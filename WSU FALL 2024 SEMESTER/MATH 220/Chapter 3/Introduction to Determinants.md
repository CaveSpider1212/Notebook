---
tags: MATH_220
created: 2024-10-15
description: Lesson 3.1 - Introduction to Determinants
---

Recall from [[Inverses]] (2.2) that we found a formula for the inverse of the matrix

$$A = \begin{bmatrix}a&b\\c&d\end{bmatrix}$$

After row reducing, we ended up with

$$A^{-1} = \frac{1}{ad - bc}\begin{bmatrix}d&-b\\-c&a\end{bmatrix}$$

where $ad - bc$ was the "determinant" of the matrix $A$.

> [!info] $A_{ij}$
> $A_{ij}$ will represent the submatrix found by deleting the $i^{th}$ row and $j^{th}$ column of the original matrix $A$.
> 
> Used to find determinants of $n$ x $n$ matrices.

> [!info] Determinant of $n$ x $n$ matrix
> For $n \ge 2$, the **determinant** of an $n$ x $n$ matrix $A = \begin{bmatrix}a_{ij}\end{bmatrix}$ is the sum of $n$ terms of the form $\pm a_{1j}$det$A_{1j}$, with plus minus signs alternating, where the entries $a_{11}, a_{12}, ..., a_{1n}$ are from the first row $A$. Symbolically,
> 
> $detA = a_{11}detA_{11} - a_{12}detA_{12} + ... + (-1)^{1 + n}a_{1n}detA_{1n}$
> 
> Can also be written as $\sum\limits_{j = 1}{n} (-1)^{1 + j}a_{1j}detA_{1j}$

> [!info] Cofactor
> Given $A = \begin{bmatrix}a_{ij}\end{bmatrix}$, the $(i, j)$-cofactor of $A$ is the number $C_{ij}$ given by
> 
> $$C_{ij} = (-1)^{i + j}detA_{ij}$$
> 
> We can now rewrite the determinant formula as $detA = a_{11}C_{11} + a_{12}C_{12} + ... + a_{1n}C_{1n}$ or equivalently in summation notation, $detA = \sum\limits_{j = 1}^{n} a_{1j}C_{1j}$
> 
> We don't actually need to use the first row...we can use any row or column.

> [!tip] Theorem
> The determinant of an $n$ x $n$ matrix $A$ can be computed by a cofactor expansion across any row or down any column. The expansion across the $i^{th}$ using the cofactor is
> 
> $$detA = a_{i1}C_{i1} + a_{i2}C_{i2} + ... + a_{in}C_{in}$$
> 
> The cofactor expansion down the $j^{th}$ column is
> 
> $$detA = a_{1j}C_{1j} + a_{2j}C_{2j} + ... + a_{nj}C_{nj}$$

The plus or minus sign in the $(i, j)$-cofactor depends on the position of $a_{ij}$ in the matrix, almost like a checkerboard.

$$\begin{bmatrix}+&-&+&...\\-&+&-& \\+&-&+& \\...& & &...\end{bmatrix}$$

> [!example]
> Find the det$A$, where
> 
> $$A = \begin{bmatrix}1&5&0\\2&4&-1\\0&-2&0\end{bmatrix}$$
> 
> (use checkerboard matrix) = $1det\begin{bmatrix}4&-1\\-2&0\end{bmatrix} - 5det\begin{bmatrix}2&-1\\0&0\end{bmatrix} + 0\begin{bmatrix}2&4\\0&-2\end{bmatrix}$
> $= 1(4 * 0 - (-1)(-2)) - 5(2 * 0 - (-1)(0)) + 0(2(-2) - 0 * 4)$
> $= -2$
> 
> det$A$ = -2

> [!tip] Theorem
> If $A$ is a triangular matrix, then det$A$ is the product of the entries on the main diagonal.