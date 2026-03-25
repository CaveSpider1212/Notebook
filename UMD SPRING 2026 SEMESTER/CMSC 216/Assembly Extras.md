---
tags: CMSC_216
created: 2026-3-24
description: 3/24 notes
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