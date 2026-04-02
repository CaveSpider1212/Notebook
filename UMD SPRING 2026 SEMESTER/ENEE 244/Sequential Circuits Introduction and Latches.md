---
tags: ENEE_244
created: 2026-3-25
description: 3/25, 3/30 notes (Slide set 11)
---

### Sequential circuits

A **sequential circuit** is one where the current output depends not only upon the current inputs, but also on past inputs. In other words, sequential circuits remember things.

This doesn't mean that we explicitly must remember any particular past inputs. Instead, this could mean that the circuit summarizes the effect of past inputs into some memory state that it stores.

![[3.25.26 Basic Sequential Circuit.png]]

### Types of sequential circuits

There are two types of sequential circuits
1. **Synchronous circuits** are a type of digital circuit where the operation is controlled by a clock signal. In these circuits, changes in the state of the circuit storage elements (like flip-flops and registers) occur at specific times, typically on the rising or falling edge of the clock pulse.
2. **Asynchronous circuits** are digital circuits that operate without a global clock signal. Instead, they rely on the changes in input signals to control the timing of state transitions. This means that components can react to input changes immediately.

Comparison:
- Synchronous circuits change state across the whole circuit in a predictable and lockstep manner, leading to easier design
	- Everybody changes at the same time
- In asynchronous circuits, each storage element changes as soon as its inputs change, which means it is a potentially faster circuit. But since different parts of the circuit can change at different times, reasoning about global behavior of the circuit is difficult.

### Advantages of synchronous circuits

- Predictable timing: The clock signal provides a clear timing reference, making it easier to synchronize operations and predict the behavior of the circuit
- Simplified design: The use of a clock simplifies the design process by providing a framework for timing control, making it easier to analyze and debug the circuit
- Deterministic behavior: The predictable nature of clock-driven state transitions reduces the likelihood of race conditions and timing-related errors, enhancing reliability
- Easier integration: Sequential circuits can be integrated with other synchronous components more easily, facilitating the design of larger digital systems like microprocessors and controllers

### Comparison to asynchronous circuits

Advantages of asynchronous circuits:
- No clock overhead: Since they do not rely on a global clock, asynchronous circuits can eliminate the power and complexity associated with clock generation and distribution
- Potential for higher speed: Asynchronous circuits can respond to changes in input signals immediately, potentially allowing for faster operation, especially in low-latency applications

Downsides of asynchronous circuits:
- Much harder to design than synchronous circuits, because of their unpredictable timing and non-deterministic behavior

Nearly all digital sequential circuits today are synchronous, including all popular CPUs used today.

### Clocked sequential circuits

A **clock signal** is an endless repeating digital signal that alternates between 1 and 0, where 1 is represented by a certain voltage value (usually a few volts, commonly 3.3V or 5V in older circuits) and 0 is represented by a voltage of around zero volts.

A synchronous sequential circuit uses circuit storage elements called **flip-flops**, each of which stores a single Boolean value (0 or 1) indefinitely while power is supplied to it.

### Flip flops vs. Latches

Flip flops and latches are both types of devices used in digital circuits to store binary data.

1. Operation Control

- **Latch**: A latch is *level-sensitive* ^5a8f27
	- Continuously responds to its input as long as the control signal (like an enable or gate signal) is active
	- Can change its output based on input as long as the control signal is in the appropriate state
	- More suitable for asynchronous circuits
- **Flip-flop**: A flip-flop is *edge-sensitive*
	- Changes its output only at specific moments, typically on the rising or falling edge of a clock signal
	- More suitable for synchronous designs

2. Timing

- **Latch**: Because latches are level-sensitive, they can introduce timing uncertainties (glitches) if the input changes while the latch is enabled, leading to potential instability
- **Flip-flop**: Flip-flops provide a more stable output because they sample the input only at defined clock edges, reducing the likelihood of glitches

Flip-flops are almost universally used as storage elements rather than latches since circuit design is much more predictable and easier with flip-flops.

On the other hand, latches are simpler to build and are used to build flip-flops.

### SR latch

S: SET
R: RESET

This is a circuit that can remember values.

- When S = 1, R = 0, then the outputs are complemented (Q = 1, Q' = 0)
	- This is called **setting** the latch (to 1)
- When S = 0, R = 1, then the inputs are complemented (Q = 0, Q' = 1)
	- This is called **resetting** the latch (to 0)
- When S = 0, R = 0, then the outputs remain the same as they were before this state
- When S = 1, R = 1, then the outputs are both driven to zero, violating the Q, Q' property
	- After this, if the outputs go to S = 0, R = 0 (the remembering state), the outputs become unpredictable
	- This is a **forbidden** input

The circuit below is level triggered, meaning it responds to inputs when input = 1 (active high). This is the first circuit covered that uses a *cycle*.

![[3.30.26 SR Latch.png]]

If S = 1, then Q' is always 0 due to the NOR gate. That means Q is always 1.

If S = 0, then the output depends on R. if R = 1, then Q = 0 by the NOR gate and Q' = 1.

If S = 0 and R = 0, then the existing values for Q and Q' go into the NOR gates and the outputs depends on those values, meaning:
- If Q = 0, then Q' becomes 1 by the NOR gate
- If Q = 1, then Q' becomes 0 by the NOR gate
- If Q' = 0, then Q is 1 by the NOR gate
- If Q' = 1, then Q = 0 by the NOR gate

If S = 1 and R = 1, then Q and Q' both become 0 by the NOR gates. However, if the circuit goes into the remembering state later on, then Q and Q' will both equal 1, and this loop will continue. The digital circuit would break.

### S'R' latch

This is similar to the SR Latch but uses NAND instead of NOR gates, and the active low (level triggered) or input = 0 latch is preferred.

![[3.30.26 S'R' Latch.png]]

The setting and resetting is exactly the opposite as an SR latch.

### SR latch with control input

This is a version of the SR latch with a control/enable input.

![[3.30.2026 SR Latch with Enable.png]]

It responds like a regular SR latch when the enable input (En) is true (1).

When En = 0, then the latch retains its previous state, because the inputs to the right half of the latch become 1, 1.

Even though it looks like an S'R' latch, it behaves just like an SR latch (the only difference is that there is an off switch).

### D Latch

D: Data

A downside of any variety of the SR latch is that it has a forbidden state.

The **D latch** eliminates this condition and prevents forbidden states from happening. The only states it has is setting, resetting, and retaining/remembering.

![[3.30.26 D Latch.png]]

This latch simply stores the value of the D input, so it's also called a **transparent latch**.

The extra NOT gate may not be needed if the input is the output of a previous latch, which will always contain Q and Q', so we wouldn't need a NOT gate to calculate Q'.