---
tags: CMSC_216
created: 2026-2-17
description: 2/17, 2/29, 2/24, 2/26 notes
---

See [[Binary Representations and Arithmetic]] and [[Special-Purpose Binary Codes]]

### Overflow

- Sums that exceed the representation of the bits associated with the integral type **overflow**
- Excess significant bits are *dropped*
- Addition can result in a sum smaller than the summands, even for two positive numbers

### Underflow

- **Underflow** occurs in unsigned arithmetic when values go below 0 (no longer positive)
- Pretend that there is an extra significant bit to carry out subtraction
- Subtracting a positive integer from a positive integer may result in a *larger* positive integer
- Integer arithmetic in fixed bits is a mathematical *ring*

### Overflow and Underflow in C Programs

- *No runtime errors* for underflow or overflow
- Good for hashing and cryptography, but bad for most other applications (should use checks for overflow/underflow)

### Integer Operations and Speed

Along with addition and subtraction, multiplication and division can also be done in binary.

Algorithms are the same as base 10 but more painful to do by hand.

The **Arithmetic and Logic Unit (ALU)** does integer operations in the machine. Typical speeds are:

|Operation|Cycles
|-|-
|Addition|1
|Logical|1
|Shifts|1
|Subtraction|1
|Multiplication|1
|Division|>30

Due to disparity, it is worth knowing about the relation between multiplication/divide and bitwise operations. The compiler often uses bit shifting rather than multiplying/dividing.

### Bitwise Operations

Logical vs. bitwise operations
```
int xl = 12 || 10; // truthy (Logical OR)
int xb = 12 | 10; // 14 (Bitwise OR)
int yl = 12 && 10; // truthy (Logical AND)
int yb = 12 & 10; // 8 (Bitwise AND)
int zb = 12 ^ 10; // 6 (Bitwise XOR)
int wl = !12; // falsey (Logical NOT)
int wb = ~12; // 3 (Bitwise NOT/INVERT)
```

Bitwise operations are evaluated on a *per-bit level*. For example, in `12 | 10`, 12 is 1100 in binary and 10 is 1010 in binary. The result would be 1110 by applying the OR operator on each individual bit from both numbers, which would be 14.

### Bitwise Shifts

**Shift** operations move bits within a field of bits

```
x = y << k; // left shift y by k bits, store in x
x = y >> k; // right shift y by k bits, store in x
```

> [!example] Shifting Examples
> ```
> char x = 0b00010111; // 23
> char y = x << 2; // left shift by 2 (y = 0b01011100 = 92)
> // x is not changed
> 
> char z = x >> 3; // right shift by 3 (z = 0b00000010 = 2)
> // x is not changed
> 
> char n = 0b10000000; // -128, signed
> char s = n >> 4; // right shift by 4 (s = 0b11111000 = -8, sign extension)
> // right shift is "arithmetic"
> ```

### Shifty Arithmetic Tricks

Shifting a number $x$ left by $k$ bits multiplies it by $2^k$. Shifting a number $x$ right by $k$ bits divides it by $2^k$.

### Checking/Setting Bits

Check if bit at position `i` is set in `x` by saying `x & (1 << i)`.

Set a bit at position `i` (set to 1) in `x` by saying `x | (1 << i)`.

Clear a bit at position `i` (set to 0) in `x` by saying `x & ~(1 << i)`.

### Byte ordering in Memory

Single bytes like ASCII characters lay out sequentially in memory in increasing address.

Multi-byte entities like 4-byte `int`s require decisions on byte ordering.

Two options for ordering multi-byte data in memory
- **Little Endian**: Least significant byte at low address
- **Big Endian**: Most significant byte at low address

Most modern machines use Little Endian ordering by default.