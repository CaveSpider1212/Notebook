---
tags: CMSC_216
created: 2026-3-5
description: 3/5, 3/10, 3/12 notes
---

### Control Flow in Assembly and the Instruction Pointer

`%rip` is the **Instruction Pointer** which contains the main memory address of next assembly instruction to execute.

After executing an instruction, `%rip` automatically updates to the subsequent instruction

### Disassembling Binaries

Binaries hard to read on their own, but we can *disassemble* binary (show "readable" version of contents) using `objdump`.

### `FLAGS`: Condition Codes Register

Most CPUs have a special register with "flags" for various conditions: each bit is T/F for a specific condition.

Bits in `FLAGS` register are *automatically* set based on results of other operations like addition, subtraction, etc.

|Bit|Abbrev.|Name|Description
|-|-|-|-
|0|CF|Carry flag|Set if last operation caused an unsigned overflow
|6|ZF|Zero flag|Set if last operation yielded a 0 result
|7|SF|Sign flag|Set if last operation yielded a negative
|8|TF|Trap flag|Used by `gdb` to stop after one ASM instruction
|9|IF|Interrupt flag|$1$: handle hardware interrupts, $0$: ignore them
|11|OF|Overflow flag|Set if last operation caused SIGNED overflow/underflow

### Comparisons and Tests

Compare: `cmpX B, A` (like `A - B`)
- Test if `A > B`

Test: `testX B, A` (like `A & B`)
- Test if `A & B`

### Jump Instructions

`jmp`: Unconditional jump (possibly to variable address)
`je` or `jz`: Equal/zero (`ZF`)
`jne` or `jnz`: Not equal/non-zero (`!ZF`)
`js`: Negative ("signed") (`SF`)
`jns`: Nonnegative (`!SF`)
`jg`: Greater-than signed (`!(SF xor OF) and !ZF`)
`jge`: Greater-than-equal signed (`!(SF xor OF)`)
`jl`: Less-than signed (`SF xor !OF`)
`jle`: Less-than-equal signed (`(SF xor !OF) or !ZF`)
`ja`: Above unsigned (`!CF and !ZF`)
`jae`: Above-equal unsigned (`!CF`)
`jb`: Below unsigned (`CF and !ZF`)
`jbe`: Below-equal unsigned (`CF`)

### Compiler Comparison Inversion

- Often compiler inverts comparisons
	- For example, `i < n` becomes `cmpX` and `jge` (jump greater/equal)
	- `i == 0` becomes `cmpX` and `jne` (jump not equal)
	- This allows the "true" case to fall through immediately

A single if-statement usually has a single jump, but having else statements may have a couple jumps.

### `call` / `ret` with Return Address in Stack

`call`:
1. Push the "caller" *return address* onto the stack
	1. Return address is for instruction after `call`
2. Change `rip` to first instruction of the "callee" function

`ret`:
1. Set `rip` to return address at top of stack
2. Pop the return address off to shrink stack

### `%rsp` is important for returns

- When a function is about to return, `%rsp` MUST refer to the memory location of the return address
- `ret` uses value pointed to `%rsp` as the return address
- Segmentation faults often occur if `%rsp` is NOT the return address: attempt to fetch/execute instructions out of bounds
- Stack is often used to store local variables, stack pointer `%rsp` is manipulated via `pushX`/`subq` instructions to grow the stack
- Before returning, MUST shrink stack and restore `%rsp` to its original value via `popX`/`addq` instructions

### Stack Alignment

Must align `rsp` (stack pointer) to 16-byte boundaries when calling functions.

`rsp` changes must be undone prior to return (so if it was changed using `subq`, must be removed using `addq`)

### x86-64 Register/Procedure Convention

![[3.5.26 Registers.png]]

Arg 7, 8: Push into the stack

**Caller save** registers: can alter these freely
- `rax`, `rcs`, `rdx`, `rdi`, `rsi`, `r8`, `r9`, `r10`, `r11`

**Callee save** registers: *must* restore these before returning
- `rbx`, `rbp`, `r12`, `r13`, `r14`, `r15`

**Stack pointer**
- `rsp`

### Caller and Callee Save Register Mechanics

Caller save registers: May all change across function call boundaries
- Not a problem for leaf functions, which don't call any other functions

Callee save registers: Have the same values in them after a function call
- Using them requires saving their original values in the stack and restoring them

### Pushing and Popping the Stack

If local variables or callee save registers are needed on the stack, can use `push`/`pop` for these.

Push and pop instructions are compound: they manipulate `%rsp` and move data in a single instruction
