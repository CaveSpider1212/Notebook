---
tags: MATH_220
description: Lesson 1.1 - Systems of Linear Equations
created: 2024-08-20
---


#### Linear Equations

- **Linear Equations**: equations that can be expressed in the forms below where b and a1, a2, ...an are real or complex numbers
  - $a_1x_1 + a_2x_2 + ... + a_nx_n = b$
  - $a_0 + a_1x_1 + ... + a_nx_n = 0$

> Examples:
> $3x_1 + 2x_2 + 5x_3 = 1$
> $x_2 = \sqrt{3}(x_1 + 5) \rightarrow -\sqrt{3}x_1 + x_2 = 5\sqrt{3}$
>
> Non-examples:
> $4x_1x_2 + x_3 = 2$
> $5x_1 + 2\sqrt{x_2} = x_3$

- **Linear Systems**: a collection of linear equations (involving the same variables)

> $x_1 + x_2 = 3$
> $x_1 - x_3 = 4$

- **Solution**: list of numbers in the form "$(s_1, s_2, ..., s_n)$"
- **Solution set**: list of all solutions in the form `{(1, 2, 3), (2, -3, 1)}` (for example)
- Two linear systems with matching solution sets are equivalent

Classifying solution sets:
![[8.20.24 Solution Sets]]

- A linear system if consistent if there is at least one solution

#### Matrices

- **Matrix**: rectangular array that compactly records information

> $$x_1 - 2x_2 + x_3 = 0$$
> $$2x_2 - 8x_3 = 8$$
> $$5x_1 - 5x_3 = 10$$
> 
> Coefficient Matrix:
> $\begin{bmatrix} 1&-2&1 \\ 0&2&-8 \\ 5&0&-5 \end{bmatrix}$
> 
> Augmented Matrix:
> $\begin{bmatrix} 1&-2&1&|&0 \\ 0&2&-8&|&8 \\ 5&0&-5&|&10 \end{bmatrix}$

- A matrix's size is written as m x n (m by n) where m is the number of rows and n is the number of columns

#### System of Equations with Matrices

- Solving systems of equations with matrices: the idea is to perform operations to the rows of the matrices to try and eliminate variables so that there is only 1 of each variable, and so that each variable has a coefficient of 1
  - These operations are called "elementary row operations"

> $3x_1 - 2x_2 + x_3 = -9$ (E1)
> $x_1 \hspace{15mm} - 5x_3 = -1$ (E2)
> $2x_1 + 2x_2 + 3x_3 = 4$ (E3)
> 
> $\begin{bmatrix} 3&-2&1&|&-9 \\ 1&0&-5&|&-1 \\ 2&2&3&|&4 \end{bmatrix}$
> 
> $3x_1 - 2x_2 + x_3 = -9$ (E1)
> $x_1 \hspace{15mm} - 5x_3 = -1$ (E2)
> $5x_1 \hspace{13mm} +  4x_3 = -5$ (E1 + E3)
> 
> $\begin{bmatrix} 3&-2&1&|&-9 \\ 1&0&-5&|&-1 \\ 5&0&4&|&-5 \end{bmatrix}$
> 
> $3x_1 - 2x_2 + x_3 = -9$ (E1)
> $x_1 \hspace{15mm} - 5x_3 = -1$ (E2)
> $\hspace{20mm} 29x_3 = 0$ (E3 - 5E2)
> 
> $\begin{bmatrix} 3&-2&1&|&9 \\ 1&0&-5&|&-1 \\ 0&0&29&|&0 \end{bmatrix}$
> 
> $3x_1 - 2x_2 + x_3 = -9$ (E1)
> $x_1 \hspace{15mm} - 5x_3 = -1$ (E2)
> $\hspace{25mm} x_3 = 0$ ($\frac{1}{29}$E3)
>
> $\begin{bmatrix} 3&-2&1&|&-9 \\ 1&0&-5&|&-1 \\ 0&0&1&|&0 \end{bmatrix}$
> 
> $3x_1 - 2x_2 \hspace{15mm} = -9$ (E1 - E3)
> $x_1 \hspace{15mm} \hspace{15mm} = -1$ (E2 + 5E3)
> $\hspace{25mm} x_3 = 0$ (E3)
> 
> $\begin{bmatrix} 3&-2&0&|&-9 \\ 1&0&0&|&-1 \\ 0&0&1&|&0 \end{bmatrix}$
> 
> $-2x_2= -6$ (E1 - 3E2)
> $x_1= -1$ (E2)
> $x_3 = 0$ (E3)
> 
> $\begin{bmatrix} 0&-2&0&|&-6 \\ 1&0&0&|&-1 \\ 0&0&1&|&0 \end{bmatrix}$
> 
> $x_1 = -1$ (E3)
> $x_2 = 3$ ($\frac{-1}{2}$E2)
> $x_3 = 0$ (E3)
> 
> $\begin{bmatrix} 1&0&0&|&-1 \\ 0&1&0&|&3 \\ 0&0&1&|&0 \end{bmatrix}$

#### Elementary Row Operations

^274143

- The elementary row operations include... ^bc66ce
  - **Replacement**: replace a row with the sum of itself and multiple of another row
  - **Scale**: multiply all entries of a row by a nonzero constant
  - **Interchange**: swap two rows

> Is this matrix consistent or inconsistent? Does it have unique solutions?
> $$\begin{bmatrix} 1&3&2&|&-1 \\ 0&1&-2&|&2 \\ 1&0&1&|&0 \end{bmatrix}$$
> 
> (R1-R3 | R2 | R3)
> $\begin{bmatrix} 0&3&1&|&-1 \\ 0&1&-2&|&2 \\ 1&0&1&|&0 \end{bmatrix}$
> 
> (R1 | R2+2R1 | R3)
> $\begin{bmatrix} 0&3&1&|&-1 \\ 0&7&0&|&0 \\ 1&0&1&|&0 \end{bmatrix}$
> 
> (R1 | 1/7R2 | R3)
> $\begin{bmatrix} 0&3&1&|&-1 \\ 0&1&0&|&0 \\ 1&0&1&|&0 \end{bmatrix}$
> 
> (R1-3R2 | R2 | R3))
> $\begin{bmatrix} 0&0&1&|&-1 \\ 0&1&0&|&0 \\ 1&0&1&|&0 \end{bmatrix}$
> 
> (R1 | R2 | R3-R1)
> $\begin{bmatrix} 0&0&1&|&-1 \\ 0&1&0&|&0 \\ 1&0&0&|&1 \end{bmatrix}$
> 
> <u>Consistent with unique solutions</u>

> Is this matrix consistent or inconsistent? Does it have unique solutions?
> $$\begin{bmatrix} 1&2&3&5&|&1 \\ 2&4&6&10&|&3 \\ 1&0&1&4&|&2 \\ 2&-1&3&2&|&0 \end{bmatrix}$$
> 
> (R1 | R2-2R1 | R3 | R4)
> $\begin{bmatrix} 1&2&3&5&|&1 \\ 0&0&0&0&|&1 \\ 1&0&1&4&|&2 \\ 2&-1&3&2&|&0 \end{bmatrix}$
> 
> <u>Inconsistent</u>

> Is this matrix consistent or inconsistent? Does it have unique solutions?
> $$\begin{bmatrix} 1&2&4&5&|&1 \\ 2&4&8&10&|&2 \\ 0&-2&-4&-8&|&-2 \\ 0&2&4&8&|&2 \end{bmatrix}$$
> 
> (R1 | R2-2R1 | R3+R4 | R4)
> $\begin{bmatrix} 1&2&4&5&|&1 \\ 0&0&0&0&|&0 \\ 0&0&0&0&|&0 \\ 0&2&4&8&|&2 \end{bmatrix}$
> 
> <u>Consistent with infinite solutions</u>

> What is the value of h that makes this system consistent?
> $$\begin{bmatrix} 1&3&|&1 \\ -2&-6&|&h \end{bmatrix}$$
> 
> (R1 | R2 + 2R1)
> $\begin{bmatrix} 1&3&|&1 \\ 0&0&|&h+2 \end{bmatrix}$
> 
> <u>h = -2</u>

> What is the value of h that makes this system consistent?
> $$\begin{bmatrix} 1&3&|&-2 \\ -2&h&|&4 \end{bmatrix}$$
> 
> (R1 | R2 + 2R1)
> $\begin{bmatrix} 1&3&|&-2 \\ 0&h+6&|&0 \end{bmatrix}$
> 
> <hr>
> <i>Case 1: h + 6 = 0</i>
> 
> $\begin{bmatrix} 1&3&|&-2 \\ 0&0&|&0 \end{bmatrix}$
> 
> $x_a + 3x_2 = -2$
> $0 = 0$
> 
> <hr>
> <i>Case 2: h + 6 != 0</i>
> 
> (R1 | 1/h+6R2)
> $\begin{bmatrix} 1&3&|&-2 \\ 0&1&|&0 \end{bmatrix}$
> 
> (R1 - 3R2 | R2)
> $\begin{bmatrix} 1&0&|&-2 \\ 0&1&|&0 \end{bmatrix}$
> 
> $x_1 = 2$
> $x_2 = 0$
> 
> <u>Consistent for all real values of h</u>
