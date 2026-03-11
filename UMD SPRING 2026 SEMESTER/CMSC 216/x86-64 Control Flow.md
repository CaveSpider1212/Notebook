---
tags: CMSC_216
created: 2026-3-5
description: 3/5, 3/10 notes
---

### Control Flow in Assembly and the Instruction Pointer

`%rip` is the **Instruction Pointer** which contains the main memory address of next assembly instruction to execute.

After executing an instruction, `%rip` automatically updates to the subsequent instruction

### Disassembling Binaries

Binaries hard to read on their own, but we can *disassemble* binary (show "readable" version of contents) using `objdump`.

### `FLAGS`: Condition Codes Register

Most CPUs have a special register with "flags" for various conditions: each bit is T/F for a specific condition.

Bits in `FLAGS` register are *automatically* set based on results of other operations like addition, subtraction, etc.