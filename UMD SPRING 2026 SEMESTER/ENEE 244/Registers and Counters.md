---
tags: ENEE_244
created: 2026-4-22
description: 4/22 notes (Slide set 15)
---

### Registers

**Register**: Collection of flip flops (usually D FFs) that stores a binary bit pattern

An N-bit register has N FFs. The N-bit pattern may represent any kind of binary data, like binary numbers for example.

##### 4-bit register w/ asynchronous reset

![[4.22.26 Register with Reset.png|200]]

Uses an active-low reset input "clear". When clear = 0, it set all FF values to 0, asynchronously at any time regardless of the clock. It is useful to initialize the register at start-up.

Downside: This register will load a new value in every cycle.

##### 4-bit register w/ parallel load and load enable

![[4.22.26 Register with Load Enable.png|400]]

All N bits can be loaded at the same time since it has parallel load (same goes for the previous register).

When load = 1, the register loads the values of I0 to I3 into the register.

When load = 0, the register retains its old value.

### Shift register

An N-bit **shift register** is a circuit that stores N bits, but upon each clock pulse, shifts its data either left or right by one position.

![[4.22.25 Shift Register.png]]

The above circuit could either be a right or left shift depending on how we assign bits to the FFs.

**Clock skew**: where different FFs can change state at different times
- Caused by intercepting clock signal with additional gates
- Could render entire sequential circuit unusable

### Serial addition

For high-end circuits like computers, we want speed. In that case, we want to add quickly, so we use [[Combinational Circuits (Adders)#^70fff9|carry-look-ahead adders]] to add multiple bits at the same time.

For low-end, human-interface circuits, we can add one bit at a time to add two N-bit numbers because it saves hardware. We would only need one full adder rather than N. This saves silicon and some leakage power consumption.

![[4.22.26 Serial Adder.png|400]]

The above serial adder adds clock skew since it has logic on the clock signal, so it is a bad idea.

**Switching power**: Power dissipated when a gate's output changes in value

**Leakage power**: Happens all the time from every gate, regardless of whether the value is switched or not

### Universal Shift Register

**Universal shift register**: Flexible shift register that can be instructed to perform a right shift, left shift, parallel load, or retain state, depending on the mode inputs.

Very useful in the arithmetic and logic unit (ALU) of a general-purpose CPU in which multiple types of instructions could be supported.

![[4.22.25 Universal Shift Register.png|400]]

![[4.22.25 Universal Shift Register Mode Table.png|400]]