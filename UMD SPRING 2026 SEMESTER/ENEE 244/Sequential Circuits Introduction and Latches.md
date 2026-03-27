---
tags: ENEE_244
created: 2026-3-25
description: 3/25 notes (Slide set 11)
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
- Potential for higher speed: Asynchronous circuits can resopnd to changes in input signals immediately, potentially allowing for faster operation, especially in low-latency applications

Downsides of asynchronous circuits:
- Much harder to design than synchronous circuits, because of their unpredictable timing and non-deterministic behavior

Nearly all digital sequential circuits today are synchronous, including all popular CPUs used today.