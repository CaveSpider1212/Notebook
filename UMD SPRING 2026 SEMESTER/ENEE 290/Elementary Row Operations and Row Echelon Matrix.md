---
tags: ENEE_290
created: 2026-3-23
description: 3/23, 3/25 notes (Lecture 14, 15)
---

### Systems of Linear Equations

> [!info] Systems of Linear Equations
> The general $m \times n$ system of linear equations is of the form
> 
> $$a_{1,1} x_1 + a_{1, 2} x_2 + ... + a_{1, n} x_n = b_1$$
> $$a_{2, 1} x_1 + a_{2, 2} x_2 + ... + a_{2, n} x_n = b_2$$
> $$...$$

A solution to the system is an ordered n-tuple of scalars $(c_1, c_2, ..., c_n)$ which, when substituted for $x_1, x_2, ..., x_n$ into the left-hand side of the equation, yields the values on the right-hand side.

The general $m \times n$ system of linear equations above can be written as a vector equation $Ax = b$.

**Hyperplane**: $\{ x \in R^n | \langle a, x \rangle = a^T x = b \}, a \neq 0$

Solution set of a system of linear equations: $S = \{ x \in R^n | Ax = b \} \subset R^n$, where $A \in R^{m \times n}$. $A_m \cdot x = b_m$ is the intersection of $m$ hyperplanes.

### Elementary Row Operations

To obtain a solution or solution set, reduce the given system of linear equations to a new equivalent system with the same solution set, but easier to solve.

$$Ax = b \rightarrow \tilde{A}x = \tilde{b}$$

Elementary row operations:
- Permute the i-th and j-th rows ($P_{i, j}$)
- Multiply the i-th row by a nonzero scalar $k \neq 0$ ($M_i (k)$)
- Add $k$ times the i-th row to the j-th row ($A_{i, j} (k)$)

Each elementary row operation is *reversible*, meaning we can undo a given elementary row operation by another one.

### Augmented Matrix

The system:
$$a_{1, 1} x_1 + a_{1, 2} x_2 + a_{1, 3} x_3 = b_1$$
$$a_{2, 1} x_1 + a_{2, 2} x_2 + a_{2, 3} x_3 = b_2$$
$$a_{3, 1} x_1 + a_{3, 2} x_2 + a_{3, 3} x_3 = b_3$$

can be written as:
$$\begin{bmatrix} a_{1,1}&a_{1, 2}&a_{1, 3} \\ a_{2, 1}&a_{2, 2}&a_{2, 3} \\ a_{3, 1}&a_{3, 2}&a_{3, 3} \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} b_1 \\ b_2 \\ b_3 \end{bmatrix}$$

The augmented matrix is:
$$\begin{bmatrix} a_{1, 1}&a_{1, 2}&a_{1, 3}&|&b_1 \\ a_{2, 1}&a_{2, 2}&a_{2,3}&|&b_2 \\ a_{3, 1} & a_{3,2} & a_{3,3} & | & b_3 \end{bmatrix}$$

### Row-Equivalent Matrix

> [!info] Row-Equivalent Matrix
> Suppose $A$ is an $m \times n$ matrix. Any matrix $B$ obtained from $A$ by a *finite sequence of elementary row operations* is said to be **row-equivalent** to $A$.

Row-equivalent augmented matrices retain the same solution set since elementary row operations don't change the solution set of a linear system.

### Row-Echelon Matrices

> [!info] Row-Echelon Matrix
> An $m \times n$ matrix is called a **row-echelon matrix** if it satisfies the following three conditions:
> 1. If there are any rows consisting of zeros, they are grouped together at the bottom of the matrix
> 2. The first nonzero element in any nonzero row is a 1 (called a *leading 1*)
> 3. The leading 1 of any row below the first row is to the right of the leading 1 of the row above it

Any matrix can be reduced to a row-equivalent row-echelon matrix by a finite sequence of elementary row operations.

> [!tip] Row Echelon Algorithm
> 1. Find the leftmost nonzero column. This is called the **pivot column**. The **pivot position** is where the leading element in that row would be.
> 2. Put 1 in the pivot position using elementary row operations.
> 3. Move the row with the pivot position to the $k$th row (where $k$ is the column)
> 4. Put 0's in the elements below the pivot position
> 5. If there is no nonzero row below the pivot position, then we are done

> [!info] Reduced Row-Echelon Matrix
> An $m \times n$ matrix is called a **reduced row-echelon matrix** if it satisfies the following conditions:
> 1. It is a row-echelon matrix
> 2. Any *column* that contains a leading 1 has zeros everywhere else

Suppose $A$ is an $m \times n$ matrix. Its row-echelon form is not unique, but its *reduced* row-echelon form is.

> [!tip] Gaussian Elimination
> Using row-echelon to solve a system of linear equations
> 
> Steps:
> 1. Construct an augmented matrix of the system
> 2. Use elementary row operations to reduce the augmented matrix to row-echelon form
> 3. Use *back substitution* to determine the solution set

**Gauss-Jordan elimination** is when the augmented matrix is reduced to *reduced row-echelon form*.

If there ends up being more variables than equations (if there is at least one row in the augmented matrix with all 0's), then there is a **free variable**. The remaining variables are determined by the system of equations and are called **bound variables**.