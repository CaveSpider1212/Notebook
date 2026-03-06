---
tags: ENEE_244
created: 2026-3-4
description: 3/4 notes (Slide set 9)
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