---
tags: CMSC_216
created: 2026-2-26
description: 2/26, 3/3, 3/5 notes
---

### The Many Assembly Languages

Most microprocessors are created to understand a binary machine language.

Machine Language provides means to manipulate internal memory, perform arithmetic, etc.

The Machine Language of one processor is not understood by other processors.

The focus in this class is the x86-64 Assembly Language.

### Assemblers and Compilers

Steps to running code (starts from source code and ends at executable machine code):
1. Preprocessing
2. Compilation (gcc or g++)
3. Assemble
4. Linking

**Compiler**: Chain of tools that translate high-level languages to lower ones, and may perform optimizations

**Assembler**: Translates text description of the machine code to binary, formats for execution by processor, late compiler stage

Consequences:
- The compiler can generate assembly code (Generated assembly is a pain to read but is often quite fast)
- A compiler on an Intel chip can generate assembly code for a different processor, called *cross-compiling*

### x86-64 Assembly Language Syntax

We will use AT&T syntax in this class.

```
multstore:
	pushq    %rbx
	movq     %rdx, %rbx
	call     mult2@PLT
	movq     %4ax, (%rbx)
	popq     %rbx
	ret
```

`%` is used to indicate registers

`q/l/w/b` is used to indicate 64/32/16/8-bit operands.

### Registers

**Registers** are memory locations directly wired to the CPU. These are usually *very* fast to access, faster than main memory.

Most instructions involve registers, access or change register value.

There are some "general purpose" registers:
![[3.5.25 Registers.png]]

### Basic Instruction Classes

Fundamentals:
- Memory movement: `mov`
- Stack manipulation: `push`, `pop`
- Addressing modes: `(%eax)`, `12(%eax, %ebx)`...

Arithmetic/Logic:
- Arithmetic: `add`, `sub`, `mul`, `div`, `lea`
- Bitwise logical: `and`, `or`, `xor`, `not`
- Bitwise shifts: `sal`, `sar`, `shr`

Control flow:
- Compare/test: `cmp`, `test`
- Set on result: `set`
- Jumps (un)conditional: `jmp`, `je`, `jne`, `jl`, `jg`, ...
- Conditional movement: `cmove`, `cmovg`, ...

Procedure calls:
- Stack manipulation: `push`, `pop`
- Call/return: `call`, `ret`
- System calls: `syscall`

Floating point operations:
- Register movement: `vmov`
- Conversions: `vcvts`
- Arithmetic: `vadd`, `vsub`, `vmul`, `vdiv`
- Extras: `vmins`, `vmaxs`, `sqrts`

### Data Movement (`movX`)

```
movX SOURCE, DEST     # move/copy source values to dest
```

This moves data from
- Register to register
- Main memory to register
- Register to main memory
- Immediate value (constant) to another location

- Variations:
	- `movq`: 64-bit (8-byte)
	- `movl`: 32-bit (4-bit)
	- `movw`: 16-bit (2-byte)
	- `movb`: 8-bit (1-byte)

### Operands and Addressing Modes

|Style|Address Mode|C-like|Notes
|-|-|-|-
|`$21`|Immediate|`21`|Value of constant
|`%rax`|Register|`rax`|To/from register contents
|`(%rax)`|Indirect|`*rax`|Register holds a memory address, so dereference it
|`8(%rax)`|Displaced|`*(rax + 2)`|Base plus constant offset, often used for struct field dereferences
|`(%rax, %rbx)`|Indexed|`*(rax + rbx) or char_arr[rbx]`|Base plus offset in given register, the actual value of `rbx` is used, NOT multiplied by `sizeof()`
|`(%rax, %rbx, 4) or (%rax, %rbx, 8)`|Scaled index|`rax[rbx]`|Like array access multiplied by `sizeof()`
|`1024`|Absolute|...|Absolute address `#1024`, rarely used

### Register Size and Data Movement

Data movement involving small registers may NOT overwrite higher bits in extended register.

Moving data to other small registers *does not alter* high bits.

### `addX`

```
addX B, A    # A = A + B
```

Addition represents most 2-operand ALU instructions well.

Second operand `A` is modified by first operand `B`. No change to `B`.

Variety of register, memory, constant combinations honored.

`addX` has variants for each register size (`addq`, `addl`, `addw`, `addb`).

Most ALU instructions follow the same pattern as `addX`.

### `leaX`: Load Effective Address

Memory addresses must often be loaded into registers. This is often done with a `leaX`, usually `leaq` in 64-bit platforms.

Sort of like the `&` operator in C but a bit more general.

### Division

Dividend must be in the `rax`/`eax`/`ax` register. The sign extend to `rdx`/`edx`/`dx` register with "preparation" instructions like `cltd`.

`idivX` takes one *register* argument which is the divisor.

At completion:
- `rax`/`eax`/`ax` holds the quotient (integer part)
- `rdx`/`edx`/`dx` holds the remainder (leftover)