---
tags: MATH_220
description: Lesson 1.2 - Row Reduction and Echelon Forms
created: 2024-08-22
---


#### Echelon and Reduced Echelon Forms

- Echelon form requirements:
  - All nonzero rows are above any rows of all zeroes
  - Each leading entry of a row is in a column to the right of the leading entry of the row above it
    - Leading entry: first nonzero entry in the row
	- All entries in a column below a leading entry are zeroes

> Example:
> $\begin{bmatrix} 2&3&4&5&|&9 \\ 0&0&5&9&|&3 \\ 0&0&0&3&|&7 \\ 0&0&0&0&|&0 \end{bmatrix}$
> 
> Non-example:
> $\begin{bmatrix} 2&3&2&1&|&4 \\ 0&0&0&-2&|&7 \\ 0&0&5&-2&|&0 \end{bmatrix}$


- Reduced echelon form additional requirements:
  - Leading entry of each nonzero row is 1
  - Each leading 1 is the only nonzero entry in the column
- Each matrix is equivalent to one and only one reduced echelon matrix

> $\begin{bmatrix} 1&3&0&0&|&4 \\ 0&0&1&0&|&5 \\ 0&0&0&1&|&6 \end{bmatrix}$
> 
> (the leading entry, or first nonzero number, in each row is 1, and that is the only nonzero entry in the column it is located in)


#### Pivots

- **Pivot position**: location in a matrix that corresponds to a leading entry in the reduced echelon form of the matrix
  - Find by reducing all entries below the leading entry to 0
- **Pivot column**: column of the matrix that contains the pivot position

- Row Reduction Algorithm
  1. Start with leftmost nonzero column (must be a pivot column with a pivot position at the top)
  2. Choose a nonzero entry in the pivot column as a pivot, and interchange rows to move this entry into the pivot position
  3. Use row replacement operations to create zeroes in all positions below the pivot
  4. "Cover" the row containing the pivot position and cover all rows above it, and apply steps 1-3 and keep repeating until there are no more nonzero rows to modify
  5. Beginning at the rightmost column and working upward and to the left, create zeroes above each pivot. If a pivot isn't 1, make it 1 using a scaling operation.
- First four steps are the "forward phase," and the fifth step (which creates the reduced row echelon form matrix) is the backwards phase

> Reduce the matrix into reduced row echelon form.
> 
> $$\begin{bmatrix}0&3&-6&6&4&-5\\3&-7&8&-5&8&9\\3&-9&12&-9&6&15\end{bmatrix}$$
> 
> (R1=R3 | R2 | R3 = R1) (*step 2*)
> $\begin{bmatrix}3&-9&12&-9&6&15\\3&-7&8&-5&8&9\\0&3&-6&6&4&-5\end{bmatrix}$
> 
> (R1 | R2-R1 | R3) (*step 3*)
> $\begin{bmatrix}3&-9&12&-9&6&15\\0&2&-4&4&2&-6\\0&3&-6&6&4&-5\end{bmatrix}$
> 
> (R1 | R2 | R3-3/2R2) (*step 4...the 2 in row 2 column 2 is the new pivot position*)
> $\begin{bmatrix}3&-9&12&-9&6&15\\0&2&-4&4&2&-6\\0&0&0&0&1&4\end{bmatrix}$
> 
> (using multiple elementary row operations...see [[Systems of Linear Equations#^274143]]) (*step 5*)
> $\begin{bmatrix}1&0&-2&3&0&-24\\0&1&-2&2&0&7\\0&0&0&0&1&4\end{bmatrix}$
> 
> Now the matrix is in reduced row echelon form.

#### Variables

- **Basic variables** are the variables corresponding to the pivot positions, and **free variables** are all of the other variables that aren't in the pivot positions (they don't have a pivot in their column anywhere)

> Determine the basic and free variables in the system of equations in the matrix.
> 
> $$\begin{bmatrix}1&0&-5&1\\0&1&1&4\\0&0&0&0\end{bmatrix}$$
> 
> $x_1 - 5x_3 = 1$
> $x_2 + x_3 = 4$
> 
> $x_1 = 5x_3 + 1$
> $x_2 = -x_3 + 4$
> 
> $x_1$ and $x_2$ are basic variables.
> $x_3$ is a free variable.

> [!tip] Existence and Uniqueness Theorem
> 
> A linear system is consistent if and only if the rightmost column of the augmented matrix is not a pivot column, that is, if and only if an echelon form of the augmented matrix has no row of the form below (b is nonzero)
>  
> $$\begin{bmatrix} 0&...&0&b \end{bmatrix}$$
> 
> If a linear system is consistent, then the solution set contains either a unique solution (no free variables) or infinitely many solutions (at least one free variable)