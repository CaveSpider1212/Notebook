---
tags: CMSC_216
created: 2026-3-24
description: 3/24, 3/26 notes
---

### Accessing Global Variables in Assembly

Global data can be set up in Assembly in `.data` sections with labels and assembler directives like `.int` and `.short`.

```
.data
an_int: # a single integer
	.int 17

some_shorts: # array of shorts
	.short 10 # some_shorts[0]
	.short 12 # some_shorts[1]
	.short 14 # some_shorts[2]

.text
accessing_globals:
	movl an_int(%rip), %eax
	leaq some_short(%rip), %rdi
```

Uses `%rip` relative addressing, taking the address of `%rip` and offsetting it by `an_int` or `some_short` bytes (see [[Assembly Basics and x86-64#^640e3f]]).

### Aggregate Data in Assembly (Arrays + Structs)

Arrays:
- Usually `base + index * size`
- Example: `movl $12, (%rdi, %rsi, 4)` for putting 12 into an integer array (stored in `%rdi`) at position `i` (`%rsi`)
- Array starting address often held in a register
- Index often in a register

Structs (pointers to structs):
- Usually `base + offset`
- Example: `movw 4(%rdi), %si` to access the second field of a struct (stored in `%rdi`) after an integer and store the value in `%si`

### Packed Structures as Procedure Arguments

Passing pointers to structs is "normal": registers contain addresses to main memory

Passing actual structs may result in *packed structs* where several fields are in a single register.

Assembly must *unpack* these through shifts and masking (shift a number of bits to the right to get to the field, then say `andX $0xFFF` or something similar to clear all bits except for the field's bits).

If a packed struct is large, it can be packed across several argument registers. At a certain size, the compiler stores very large structs in the stack and passes it as pointers to it to functions.

### General Cautions on Structs

- Struct layout by compiler
	- The compiler honors the order of source code fields in the structs, but it may add padding between/after fields for alignment
	- As a result, the compiler determines the total struct size
- Struct layout algorithms
	- Baked into the compiler
	- May change from compiler to compiler
	- May change through history of compiler
- Structs in memory/register
	- Local variables structs spread across several registers
	- Don't need a struct on the stack at all in some cases
	- Struct arguments packed into 1+ registers

### Security Risks in C

- Buffer overflow attacks
	- No default bounds checking in C: performance favored over safety
	- Allows classic security flaws; for example, if we have a buffer of size 1024, but a data larger than the buffer is written in it, then the program begins overwriting other parts of the stack
		- Clobber return addresses
		- Insert executable code and run it
- Counter-measures
	- Stack protection is default in `gcc`
	- Insert "canary" values on the stack near return address, and prior to the function return, check that the canary values remain unchanged