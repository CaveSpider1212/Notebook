---
tags: CMSC_216
created: 2026-4-9
description: 4/9 notes
---

### The Process Table

- OS maintains data on all processes in a **process table**
- Process table entry ~~ process control block
- Contains info like PID, instruction the process is executing, virtual memory address space, and files in use

### File Descriptors

- Each process table entry contains a table of open files
- A use program refers to these via **file descriptors**
- File descriptor is an integer index into Kernel's table
- File descriptor table entry refers to other Kernel/OS data structures

### File Descriptors are Multi-Purpose

- Unix tries to provide most things via files/file descriptor (FD)
- Many Unix system actions area handled via `read()`-from or `write()`-to FDs
- FDs allow interaction with "normal" files to read/change them
- FDs also allow interaction with many other things
	- Pipes for interprocess communication
	- Sockets for network communication
	- Special files to manipulate terminal, audio, graphics, etc.
	- Raw blocks of memory for shared memory communication
	- Even processes themselves have special files in the file system

### Open and Close: File Descriptors for Files

`open()` and `close()` show common features of many system calls.

- Returns -1 on errors
- Show errors using the `perror()` function
- Use of `|` to bitwise-OR several options

### `read()` from File Description

`read()`:
- Read up to `SIZE` (defined constant) from an open file descriptor
- Bytes stored in `buffer` (a character array), overwrite it
- Return value is number of bytes read, -1 for error

Caution:
- Bad things happen if `buffer` is actually smaller than `SIZE`
- `read()` does NOT null terminate, so add `\0` manually if needed