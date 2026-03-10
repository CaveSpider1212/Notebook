---
tags: ENEE_244
created: 2026-3-4
description: 3/4, 3/9 notes (Slide set 9)
---

### Combinational circuits

A **combinational circuit** is a digital circuit with gates where the output depends only on the current inputs. In other words, there is no dependence on past inputs, meaning these circuits have no storage, and cannot remember anything.

Circuits that do remember are called [[Boolean Algebra#^ab8de8|sequential circuits]].

Note that a combinational circuit only produces the correct output during the time that the inputs are held steady.

Moreover, the correct output appears a certain amount of time *after* the inputs first appear. This time is called the **propagation delay** of the circuit, which results from propagation delay of the gates within it.

### Half adder

A **half adder (HA)** is a digital circuit that adds two single-bit binary numbers together to produce a sum and a carry. It's inputs and outputs are:
- Inputs: Two inputs (x, y), which are the two bits to add
- Outputs: Two outputs, a sum (S) and a carry (C), resulting from adding the two inputs

$$C = x \cdot y$$
$$S = x \oplus y$$

|$x$|$y$|$C$|$S$
|-|-|-|-
|0|0|0|0
|0|1|0|1
|1|0|0|1
|1|1|1|0

![[3.4.26 Half Adder.png]]

### Full adder

A **full adder** is a circuit that recognizes that to add two numbers, for each bit other than the least significant, we need to add three bits, not two.

The three bits are $x$ and $y$ for the bits from the two numbers we are adding in this bit position, and the carry from the previous bit.

This circuit essentially adds three bits instead of two.

|$x$|$y$|$z$|$C$|$S$
|-|-|-|-|-
|0|0|0|0|0
|0|0|1|0|1
|0|1|0|0|1
|0|1|1|1|0
|1|0|0|0|1
|1|0|1|1|0
|1|1|0|1|0
|1|1|1|1|1

### Minimizing the full adder

Using K-maps, we get the following Boolean formulas:

$S = x'y'z + x'yz' + xy'z' + xyz$
$C = xy + xz + yz$

Unfortunately, the resulting circuits are large.

### 4-bit full adder (ripple carry adder)

We can implement a N-bit adder by cascading N full adders.

The reason this works is that we are adding $A_i + B_i + C_i$ at each stage with the full adder at that stage. We can build larger adders by cascading 4-bit ripple carry adders (for example, 8 4-bit adders yields a 32-bit adder).

### Why ripple carry adders are slow

The propagation time for a ripple-carry adder is N x D, where N is the number of bits and D is the propagation delay of a single full adder. This can be far too slow for large values of N, like 32 or 64, used in modern computers.

### How to build a faster adder: mathematics

We can build a faster adder by calculating the carries for each stage directly from the inputs, instead of from the previous stage.

$C_{i + 1} = G_i + P_i C_i$, where $P_i = A_i \oplus B_i$ and $G_i = A_i \cdot B_i$

$P_i$ and $G_i$ can be computed at each bit very quickly, without using the input carry from the previous stage.

Now we can express $C_1, C_2, ...$ directly by expanding the carry equation above successively. These are two-level circuits, which are a faster way of computing carries directly from available inputs without using previous carries.

This is called **carry look ahead**, which results in a faster circuit for addition.

Carry look ahead (CLA) adders are often used in circuits, but if it is used directly for a large number of bits like 32, then a lot of logic and therefore silicon area is needed, so 4-bit or 8-bit CLA modules are common to reduce the amount of logic.



