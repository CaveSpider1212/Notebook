---
tags: ENEE_244
created: 2026-4-1
description: 4/1, 4/8 notes (Slide set 12)
---

### Why we need flip flops

Latches are undesirable because they are [[Sequential Circuits Introduction and Latches#^5a8f27|level triggered]].

In many circuits, the output of one latch is the input to the next latch, meaning when the first latch starts changing state, it is no longer holding the output steady for the next latch, making the outputs of the next latch unpredictable.

Synchronous circuits rarely use latches. Instead, we design **flip flops**, which are *edge-triggered* storage elements:
- There are two types of flip flops, positive- and negative-edge triggered
- The flip flop captures the value of the input that was present just before the rising edge or just below the falling edge, for positive- and negative-edge triggered flip flops respectively
- The inputs to each stage are held steady for the next stages throughout the cycle, so this behavior is ideal

### Master-slave flip flop (D flip flop)

A **master-slave** flip flop is a *negative-edge triggered* FF.

![[4.1.26 Master-Slave Flip Flop.png]]

The master enable is the clock signal (CLK), and the slave enable is the CLK', meaning only one of them is enabled at once:
- When CLK = 1, the master changes value (so the input D is stored in the master), but the slave holds the previous value of the master since it's disabled (meaning the output from the master, Y, is not stored in the slave)
- When CLK = 0, the master holds its value and the slave gets that value (meaning the output from the master, Y, is stored in the slave)
- This means the output changes only when CLK changes from 1 to 0, a negative edge, and this is the only time the output changes.
- The input is reacted to when CLK = 1 in a cycle, but is reflected in the slave in the next cycle

Uses 9-11 gates total (4-5 for each latch)

![[4.8.26 D Flip Flop Negative Edge.png|300]]

### An alternate (smaller) edge-triggered D flip-flop

![[4.1.26 D Flip Flop.png|400]]

This has 6 gates, which is less than the master-slave FF, and has 3 SR latches.

This is a *positive-edge triggered* FF.

- When CLK = 0, the S and R inputs are both driven to 1, which puts the S'R' latch on the right in a *remember state*
- Afterwards, when CLK goes to 1, then the clock no longer affects the two S'R' latches on the left. Then, if D = 0 when CLK becomes 1 (S was 1), then R changes to 0
	- This is the *reset state* for the third latch, making Q = 0
	- If there is a change to the D input while CLK = 1, R remains 0 because Q = 0, so the FF is a positive-edge triggered FF
- When CLK goes to 1, if D = 1 at the positive edge, then S goes to 0, because R was 1 and remains 1.
	- This puts the FF in a *set state*, making Q = 1
	- Any changes in D while CLK = 1 does not affect the output

All memory is designed using this circuit.

![[4.8.26 D Flip Flop Positive Edge.png|300]]

Characteristic table for D flip flops:
![[4.22.26 D Flip Flop Table.png]]

### Setup and hold times

For the D edge-triggered flip flop to work properly, there needs to be:
- **Setup time**: Minimum time during which the D input must be held steady *before* a triggering clock edge
- **Hold time**: Minimum time during which the D input must be held steady *after* a triggering clock edge

These times are required so that the values are held steady for long enough that the output appears properly and for long enough to result in the desired state transition at the output.

As long as the clock cycle time is greater than  the sum of the propagation delay and the setup time, then the setup time constraint is true.

The output of the D flip flop shouldn't change too quickly to satisfy the hold time constraint.

### JK flip flop

A flip flop can perform three operations: set, reset, and complement the stored value, in addition to the "remember" function.

The D flip flop is the most area efficient (and the most commonly used), but it only supports set and reset via its single input.

The JK flip flop allows for complementing as well.

![[4.1.26 JK Flip Flop.png]]

### Truth tables vs. function tables vs. characteristic tables

Truth tables:
- Combinational circuits only
- Maps constant inputs to outputs
- Usually $2^n$ rows, where $n$ is the number of inputs

Function tables:
- Combinational or sequential circuits
- May not contain all inputs
- Outputs may be defined in terms of current state (in sequential circuits)
- Fewer rules

Characteristic table:
- Synchronous sequential circuits only
- Enumerate all possible inputs, and shows next state in terms of current state
- May also show any outputs of the circuits, but not present for flip flops

### T flip flops

A **T flip flop** supports the complement function, but not the set and reset functions. T stands for "toggle", meaning "change the state to the complement of the current state".

![[4.8.26 T Flip Flop Table.png]]

A T flip flop can be build using either a JK flip flop or a D flip flop. The latter is more area-efficient.

![[4.8.26 T Flip Flop.png]]

### Characteristic equations

A **characteristic equation** expresses the output(s) of a sequential circuit as a Boolean expression of the current state and the inputs, based on what is on the characteristic table.

For D flip flops: $Q(t + 1) = D$

For JK flip flops: $Q(t + 1) = JQ' + K'Q$

For T flip flops: $Q(t + 1) = TQ' + T'Q$

### D flip flop with asynchronous reset

A flip flop may have an asynchronous reset, meaning it has an input which resets the state at any time independent of the clock.

It is useful to initialize a circuit upon its first startup (otherwise, a flip flop will have an undefined value at startup).