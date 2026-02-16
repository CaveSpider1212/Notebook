---
tags: ENEE_244
created: 2026-2-11
description: 2/11, 2/16 notes (Slide set 5)
---

### How many functions are there of $n$ variables?

Each function has $2^n$ rows in its truth table.

This means there are $2^{2^n}$ functions of $n$ variables since each number in the output column could be either 0 or 1.

### Logic gate circuit symbols

> [!info] Logic Gates
> |Name|Graphic symbol|Algebraic function|Truth table description
> |-|-|-|-
> |AND|![[2.16.26 AND Gate.png]]|$F = x \cdot y$|True when both inputs are true
> |OR|![[2.16.26 OR Gate.png]]|$F = x + y$|True when either input is true
> |Inverter (NOT)|![[2.16.26 NOT Gate.png]]|$F = x'$|True when input is false
> |Buffer|![[2.16.26 Buffer Gate.png]]|$F = x$|True when input is true
> |NAND ("Not AND")|![[2.16.26 NAND Gate.png]]|$F = (xy)'$|True when either input is false
> |NOR ("Not OR")|![[2.16.26 NOR Gate.png]]|$F = (x + y)'$|True when both inputs are false
> |XOR (Exclusive-OR)|![[2.16.26 XOR Gate.png]]|$F = xy' + x'y = x \oplus y$|True when only one input is true
> |Exclusive-NOR|![[2.16.26 Exclusive-NOR Gate.png]]|$F = xy + x'y' = (x \oplus y)'$|True when both inputs are either both true or both false

### Universality of NOR and NAND

AND, OR, and NOT can all be replaced in terms of NOR. The same goes for NAND.

This means both NOR and NAND are **universal gates**, meaning that they alone can be used to build all Boolean circuits.

### Multi-input gates

AND and OR gates can have multiple inputs with no problem since they are commutative and associative.

NOR and NAND are not associative, so to have multiple input NOR/NAND gates, we need to define them something like $F = (x + y + z)'$ and $F = (xyz)$ respectively.

The intuition for a multi-input XOR gate is that, regardless of the number of inputs, if the number of inputs true is odd, it is *true*.
- This is the definition of [[Special-Purpose Binary Codes#^55455f|even party]], making XOR useful for calculating EVEN parity bits
- XNOR is good for a parity bit for ODD parity


### Don't-care Conditions

In certain problems, some outputs are not specified, and they can be either 1 or 0. They are called **don't care conditions**, denoted by "X" or sometimes "d."

Such functions are represented separately in the minterm canonical form