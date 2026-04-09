---
tags: ENEE_244
created: 2026-3-11
description: 3/11, 3/23, 3/25 notes (Slide set 10)
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

The above circuit for calculating $G_i$ using $G_{i - 1}$ is slow (just like a ripple-carry adder), so we need to directly calculate $G_i$.

$(A > B) = a_3 b_3' + x_3 a_2 b_2' + x_3 x_2 a_1 b_1' + x_3 x_2 x_1 a_0 b_0'$
$(A < B) = a_3 ' b_3 + x_3 a_2' b_2 + x_3 x_2 a_1' b_1 + x_3 x_2 x_1 a_0' b_0$

### Decoders

A **decoder** is a circuit with $n$ inputs and $m$ outputs, where usually $m = 2^n$. These are called $n$ to $m$ ($n \times m$) decoders.

Let $n$ inputs taken together in binary represent the number $k$ in binary format. Then, $i = 1$ if $k = i$ and $i = 0$ if $k \neq i$. In other words, the output $i$ is 1 if input is $i$.

Possible uses:
1. When there is an N-bit encoding used to activate 2^N possible actions
2. Decoders can be used to implement any function
	1. Simply OR together the minterms present in the function's sum of products canonical form
		1. K-maps are still better since it yields a smaller circuit, but it can be useful when no custom silicon is available as decoders could be purchases, so this yields cheaper and smaller electronics
	2. Alternatively, take NOR of minterms not in function

### A 2 to 4 reverse output decoder with enable input

A **reverse output decoder** is a decoder where the output is reversed (When the input is $i$, the $i$th output is 0, and the rest are 1).

Often economical to build using NAND gates, which are easier to build than AND gates in certain technologies.

A decoder with an **Enable input** is one where an enable input $E$ is present, where if $E = 1$, then the function is like a decoder, but if $E = 0$, then all outputs become 0 ("turning off" the decoder).

Using AND gates instead of NAND would have produced a regular decoder, so a NAND gate produces a reverse output decoder.

### Building larger decoders from smaller ones

We can build a decoder with $N + 1$ inputs using two decoders each with $N$ inputs.

### Encoders

An **encoder** performs the inverse operation of a decoder.

A $2^N$ to $N$ encoder is one which has $2^N$ inputs and $N$ outputs. It assumes only one of the inputs is 1 at any one time, and the rest are zero.

In that case, if the $i$th input is 1, then the output is the binary number $i$.

![[3.23.26 Regular Encoder.png]]

V means at least one of the inputs was 1.

A regular encoder is rarely used since it has undefined outputs for most input combinations (those in which more than one input is 1). Priority encoders are typically used instead.

### Priority encoders

A **priority encoder** is one which allows for the possibility that inputs might be in contention, meaning more than one input bit might be 1.

In this case, it considers only the input bit of the highest priority among the inputs that are 1.

4 to 2 priority encoder:
![[3.23.26 Priority Encoder Circuit.png]]

How to design larger priority encoders:
- It is harder to design larger priority encoders using K-maps
- It is possible to build larger priority encoders using smaller ones.
- Divide the $n$ inputs into smaller groups that match the size of the smaller $m$-bit priority encoders.
- Use additional logic (OR gates) to determine which group has the highest priority

### Multiplexers

A **multiplexer** is a circuit that has two sets of inputs:
- $2^n$ data inputs ($I_0$ to $I_{2^n - 1}$)
- $n$ select inputs ($S_0$ to $S_{N - 1}$)

It has the following output:
- A single bit $Y$, that is the value of $I_S$, where is is the number $S_{N - 1}...S_0$

It sends the $S$th data input to the output. This is abbreviated as "mux."

Muxes act as electronic selectors, and are useful for that purpose in a variety of circuits.

![[3.23.26 Mux.png]]

### Multi-bit multiplexers

A *multi-bit* mux selects among groups of several bits (called words) using the *same* select inputs. It outputs one word instead of one bit.

It outputs the $S$th input word, where $S$ is the shared select input.

### Implementing a Boolean function with a mux

A mux can also be used to implement any Boolean function like decoders
- Advantage: muxes need no extra hardware (unlike decoders, which need extra OR gates at the output)
- Disadvantage: A mux can implement only one Boolean function of the same inputs at one time, unlike a decoder

This is done by making the function inputs the select bits, and the output values of the function the data inputs into the mux.

### Demultiplexers

A **demultiplexer** is the opposite of a multiplexer.

Inputs:
- A single data bit $D$
- A $n$-bit select input $S$

Outputs:
- $2^n$ data outputs

A demux outputs bit $D$ to the $S$th output.

A demux is identical to a decoder with enable input, where the enable input is called the data input instead. If $E = 1$, then it outputs 1 to the $S$th output. If $E = 0$, then it outputs 0 instead.

### MSI Logic Blocks

MSI stands for medium scale integration.

Blocks like adders, comparators, decoders, multiplexers, and flip-flops can be used in two ways:
- Inside a larger custom chip
- As standalone MSI logic chips bought from a vendor

These are real commercial parts, not just textbook ideas.

Why use MSI chips?
- If only a small fixed logic function is needed, a standard chip is much cheaper and faster than custom silicon.
- Custom silicon can have a very high one-time design cost, so using MSI chips avoids that expense.

### Why MSI chips are still used today

MSI chips are still used as glue logic around processors, memories, sensors, and peripheral devices, helping connect and coordinate parts of a digital system.

They are also used in small embedded products, older legacy systems, labs, and prototypes, where one simple standard chip may solve the problem at lower cost and lower risk than custom silicon.

A full mother board is usually not needed.

For labs and early prototypes, these chips can be placed on a breadboard or a simple printed circuit board.

For a real product, a custom printed circuit board is actually used, and it is much cheaper than creating custom silicon.