---
tags: ENEE_244
created: 2026-3-11
description: 3/11 notes (Slide set 10)
---

### Magnitude comparators

A **magnitude comparator** is a circuit that takes two $n$-bit positive binary numbers $A$ and $B$, and returns whether $A > B$, $A = B$, and $A < B$ are each true or false (only comparing the size/magnitude of the numbers, which are assumed to be positive).

The inputs are $A = a_n ... a_1$ and $B = b_n ... b_1$.

> [!tip] Equality Comparison
> $x_i = 1$ if $a_i = b_i$
> 
> $x_i = a_i b_i + a_i' \cdot b_i'$ (XNOR)
> 
> $A = B$ is $x_n \cdot x_{n - 1} \cdot ... \cdot x_1$ (just AND all the $x$ values)

> [!tip] Greater Than and Less Than (Recursive)
> $A_i > B_i$ if $(a_i > b_i)$ or ($(a_i == b_i)$ and $(A_{i - 1} > B_{i - 1})$)
> 
> $G_i = A_i > B_i$
> $G_i = a_i b_i' + x_i G_{i - 1}$
> 
> Base case: $A_0 > B_0 = a_0 \cdot b_0'$

![[3.11.26 Magnitude Comparator.png]]

### Cascade (ripple) comparator

The above circuit for calculating $G_i$ using $G_{i - 1}$ is slow, so we need to directly calculate $G_i$.

$(A > B) = a_3 b_3' + x_3 a_2 b_2' + x_3 x_2 a_1 b_1' + x_3 x_2 x_1 a_0 b_0'$
$(A < B) = a_3 ' b_3 + x_3 a_2' b_2 + x_3 x_2 a_1' b_1 + x_3 x_2 x_1 a_0' b_0$

### Decoders

A **decoder** is a circuit with $n$ inputs and $m$ outputs, where usually $m = 2^n$. These are called $n$ to $m$ ($n \times m$) decoders.

Let $n$ inputs taken together in binary represent the number $k$ in binary format. Then, $i = 1$ if $k = i$ and $i = 0$ if $k \neq i$. In other words, the output $i$ is 1 if input is $i$.

Possible uses:
1. When there is an N-bit encoding used to activate 2^N possible actions
2. Decoders can be used to implement any function
	1. Simply OR together the minterms present in the function's sum of products canonical form
	2. Alternatively, take NOR of minterms not in function