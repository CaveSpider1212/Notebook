---
tags: ENEE_244
created: 2026-4-8
description: 4/8, 4/13 notes (Slide set 13, part of 14)
---

Analysis of a clocked synchronous sequential circuit is the process of understanding what a given circuit of this type does.

### Analysis with D flip flops

Example D flip flop circuit:
![[4.8.26 D Flip Flop Example Circuit.png|400]]

We can derive **state equations** from the circuit, which express the next state and outputs from the current state.

The state equations from the figure above:
- $A(t + 1) = A(t) x(t) + B(t) x(t) = Ax + Bx$
- $B(t + 1) = A'(t) x(t) = A'x$
- $y(t) = (A(t) + B(t)) \cdot x'(t) = (A + B)x'$

### State table

We can generate a **state table** from the state equations. They look like a truth table, but they express the next state and outputs in terms of the current state and inputs.

In state tables, we list the rows as all possible combinations of the present state and inputs (in the previous example, $A$ and $B$ along with $x$), then the next state and output are calculated using the state equations and the present state and input values.

The resulting state table for the example D flip flop circuit and state equations is:
![[4.8.26 D Flip Flop Example State Table.png|400]]

Below is an alternate version of the state table, where the input combinations are of the current state bits only:
![[4.8.26 D Flip Flop Example Alternate Table.png|400]]

### State diagram

We can derive a **state diagram** from the state table, which is just a [[Graphs|graph]], where the input combinations of all possible states are the nodes and the state transitions are the edges between the nodes.

Each edge is labeled by 2 numbers I/O, where I is the input combination and O is the output combination. The direction of the edges are from the current state to the next state.

From each state, the number of outgoing edges = the number of input value combinations. In this case, $x$ can take on two values (0 and 1), so 2 outgoing edges for each state.

![[4.8.26 D Flip Flop Example State Diagram.png|400]]

This circuit outputs a 1 in the cycle when it sees a 0 in the input that follows at least one 1.

### Mealy and Moore machines

Mealy and Moore machines are two types of clocked sequential circuits:
- In a **Mealy machine**, the output is a function only of the current state and input
	- In a state diagram, the output is shown on the edges, because it depends on the current input shown on that edge
- In a **Moore machine**, the output is a function of the current state only
	- In a state diagram, the output is invariant of the inputs, and hence can be shown inside of the states

### An advantage of Moore circuits

In Mealy machines:
- If inputs are used to calculate next state, then there may be momentary false outputs.
- Solution: The circuit should sample outputs only during when we know they are correct. We also need to synchronize input changes with the clock. Finally, we may need to sample the output only at an edge trigger.

Moore machines do not have this problem.