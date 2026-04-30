---
tags: CMSC_216
created: 2026-4-23
description: 4/23, 4/30 notes
---

**Virtual Memory**: OS somehow prevents programs from "getting" the same memory addresses

### Paged Memory

- Physical devices divide memory into chunks called **pages**
- Common page size supported by many OS's (Linux) and hardware is 4KB (4096 bytes)
- CPU models use some number of bits for **virtual addresses**

There is a page table created for each process.

### Translation

Within a page, the addresses are sequential. Between pages, the addresses may be non-sequential.

Translation must be fast, so involves special hardware.

**Memory Manager Unit (MMU)** is a hardware element specifically designed for address translation. It usually contains a special cache, **Translation Lookaside Buffer (TLB)**, which stores recently translated addresses.

OS kernel interacts with MMU.

### Trade-offs

Wins:
- Avoids memory conflicts where separate programs each use the same memory address
- Programs can be compiled to assume they will have all memory to themselves
- OS can make decisions about DRAM use and set policies for security and efficiency

Losses:
- Address translation is not in constant time, has an impact on performance of real algorithms
- Requires special hardware to make translation fast enough (MMU/TLB)
- Not needed if only a single program is running on a machine

### `mmap()`

`mmap()` creates new entries in the page table

`munmap()` deletes entries in the page table

We can request a specific address in the `mmap()` call, or we can let the OS choose the address by saying `NULL`.