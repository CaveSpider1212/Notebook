---
tags: ENEE_244
created: 2026-2-2
description: 2/2, 2/4, 2/9 notes (Slide set 3)
---

### Motivation

**Boolean algebra** is a branch of math dealing with logical operations using binary variables, which can either be "true" (1) or "false" (0).

It is the foundation behind designing all binary digital circuits. The two types are:
- Combinational circuits: Those whose output depends only on the current inputs
- Sequential circuits: Those whose output depends on current and past inputs ^ab8de8
	- Circuits that remember

Computers require both types of circuits. Combinational circuits are in charge of math and logic functions, while sequential circuits handle registers and memory.

### Designing combinational circuits

A **mathematical algebra** consists of:
- A set of elements
- A set of operators
- A number of postulates/axioms: assumed to be true without proof

### Properties of operators in a set $S$

- An operator is said to be **closed** if for every pair in $S$, the operator maps to an element in $S$ (ex: addition is closed for natural numbers)
- An operator $\times$ is said to be **associative** if $(x \times y) \times z = x \times (y \times z)$ (for example)
- An operator $\times$ is said to be **commutative** if $x \times y = y \times x$ (for example)
- An identity element $e$ exists for an operator $\times$ if $\exists e \in S$ such that $\forall x \in S$, $e \times x = x \times e = x$ (for example)
- An operator $\times$ is said to distribute over $+$ if $x \times (y + z) = (x \times y) + (x \times z)$ (an example...not always the case that one operator distributes over another)
- An operator $f$ is said to have an inverse if $\forall x, y \in S, f(x, y) = z$, then $f'(z) = x$, and $f''(z) = y$. Here, $f'$ and $f''$ are inverse operators of $f$.

### Boolean algebra

The set is $S = \{ 0, 1 \}$.

There are three operators, called [[Introduction to Propositional Logic#^27f6d3|logical operators]]:
- AND ($\cdot$)
- OR ($+$)
- NOT ($'$)

Logical operators have [[Truth Tables|truth tables]], which define what those operators do.

### Axioms for Boolean algebra

- All 3 logical operators are closed, since the result can either be 0 or 1 always
- Both $+$ and $\cdot$ are *associative* and *commutative*
- The identity of $+$ is 0, while the identity of $\cdot$ is 1
- AND and OR have no inverses, while NOT is its own inverse
- Both AND and OR distribute over the other

> [!info] Distributive Law of OR over AND
> $$X + YZ = X + (Y \cdot Z) = (X + Y)(X + Z)$$

### Duality

**Duality**: Replace $+$, $\cdot$ by the other, and flip $0, 1$, then the result remains true

For example, $x + x = x$ and $x \cdot x = x$ are both true, and $x + 1 = 1$ and $x \cdot 0 = 0$ are both true.

### Operator precedence

In whole number algebra, the acronym PEMDAS is used for operator precedence.

In Boolean algebra, the order of precedence is Parentheses, NOT, AND, OR.

### Boolean functions

A **Boolean function** is any expression using Boolean variables and operators.

We can construct a truth table from the function by filling in the different possible values for each variable (0 or 1).

Using the results of a truth table, we can also derive a Boolean function by taking the values of the input variables when the output variable is true (1).

### Boolean simplification

1. Algebraic manipulation: Using algebra (distribution, commutative, etc.)
2. Boolean minimization: More systematic and guaranteed to reach minimum size expression