---
tags: CMSC_132
created: 2025-11-19
description: 11/19 notes (Lecture 33)
---

### Processes

A **process** is a program loaded into memory and executing.

Processes have their own independent *address space*, meaning its own region of memory with its own variables and data structures.

Each process may be executing a different program.

If processes need to communicate they can do so via the operating system, files, and the network.

### Threads

A **thread** is a sequentially-executed sequence of instructions inside a process (running concurrently in their process).

Threads share an address space (data) with other threads in the same process.

Each thread has its own execution context, meaning its own runtime stack (local variables).

Threads communicate via shared access to data.

Multiple threads in a process execute the *same* program.