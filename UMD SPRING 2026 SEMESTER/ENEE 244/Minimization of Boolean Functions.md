---
tags: ENEE_244
created: 2026-2-12
description: 2/16, 2/18, 2/23 notes (Slide set 6)
---

### Boolean simplification

Simplification is important because:
- Less silicon area (due to less gates and smaller circuit) means a lower cost
- Usually less power consumption, so batteries last longer
- Usually faster circuit

### Criteria for minimality assumed

A minimal formula is a *normal form* formula containing a minimum number of gate inputs.

Size to be minimized = number of literals in the formula + number of terms in the formula

### Method for minimization

The **Karnaugh Map** (K-map) is a method used to minimize Boolean formula to their provably minimum size form.

Each cell in a K-map represents a minterm, and each row and column represents one value of one variable (for 2-variable K-maps).

### Minimization procedure

1. For a given function, fill in cells in the K-map where the function is true with 1
2. Group together all the 1's in the k-map into a minimum number of maximum-size rectangles. The rectangles must NOT contain any zeros.
	- Each rectangle is made of adjacent cells only, and must have a power-of-two number of squares.
	- The reason we want maximum-size rectangles is because the larger the rectangle size, the smaller its resulting term
3. Write down resulting expression as sum of terms for each rectangle. The term for each rectangle is the product of variables that do not vary in it. This yields the minimized function.
