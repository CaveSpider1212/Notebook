---
tags: ENEE_244
created: 2026-4-13
description: 4/13, 4/15, 4/20 notes (Slide set 14)
---

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

### Design of sequential circuits (opposite of analysis)

1. Create a precise English description
2. Decide the number and nature of states
3. Draw state diagram
4. Minimize states (not in syllabus)
5. Decide number of flip flops (usually $\lceil \log_2$ \(# of states) $\rceil$)
6. Assign the states to bit patterns (**state assignment**)
7. Draw state table
8. Choose the type of flip flops to use (D when inputs become the state, T when toggling is required, JK for general, more complex circuits)
9. From state table, derive the excitation table using the flip flop excitation tables
10. Obtain flip flop input and circuit output functions
11. Minimize flip flop input and circuit output functions
12. Draw the circuit

### Obtaining FF input and circuit output functions (for D flip flops)

The equations for the flip flop inputs and circuit outputs (in terms of the current state and inputs) can be derived from the state table by listing the minterms which are 1 for that next state or output column.

### Excitation Tables

For flip flops other than D flip flops, the FF input functions are not directly available from the state table, so we need an **excitation table**, where the states (current and next states) are the inputs and the values of the FF inputs are the outputs.

![[4.20.26 Excitation Tables.png]]