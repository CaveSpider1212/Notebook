---
tags: ENEE_244
created: 2026-2-9
description: 2/9, 2/11 notes (Slide set 4)
---

### Normal form

A **normal form** (also called standard form) of a Boolean function is any
- Sum of products of Boolean variables
- Product of sums of Boolean variables

You can obtain the normal form using Boolean simplification.

Normal forms are not unique.

### Canonical form

Canonical forms are a unique way of defining a function. Unlike a normal form, there is *only one* canonical form for every function (and vice-versa).

**Minterm** or **standard product**: A product of variables and complemented variables (ex: $xy$, $xy'$)

**Maxterm** or **standard sums**: A sum of variables and complemented variables (ex: $x + y' + z$)

Each row of the truth table has a minterm and maxterm (starts from $m0$ for minterms and $M0$ for maxterms and increases for each row).

### Representing Boolean functions using minterms

Take the sum of all the terms (minterms) whose function output value is 1.

This would be called the **minterm canonical form** and is unique to the function.

### Representing Boolean functions using maxterms

Take the product of all the terms (maxterms) whose function output value is 0.

This would be called the **maxterm canonical form** and is also unique for the function.

### Gates

Each of the three elementary Boolean functions (AND, OR, NOT) have a physical semiconductor device that can implement it, called **gates**.

AND gate:
![[2.11.26 AND Gate.png]]

OR gate:
![[2.11.26 OR Gate.png]]

NOT gate:
![[2.11.26 NOT Gate.png]]

Gates are the building blocks of circuits. They are built using semiconductor elements called **transistors**.

### Boolean formulas and combinational circuits

**Analysis procedure**: This is a method for converting circuits with gates into formulas, which involves going left-to-right on the circuit and writing down the expression at each output until we reach the entire circuit's output

**Synthesis procedure**: This is a method for converting a formula to a combination circuit, which involves continuously drawing gates for each sub-expression in the formula in the correct precedence order.

When we simplify a Boolean formula, we simplify the circuit as well.