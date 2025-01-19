---
tags: CPT_S_122
created: 2025-1-12
description: Lesson 1.2
---

### What is a Data Structure?

- **Data structure**: software construct describing the organization and storage of information
	- Designed to be accessed efficiently
	- Composite of related items
- Defined and applied for particular applications and/or tasks

### Basic Applications of Dynamic Data Structures

- **Lists** are collections of data items lined up in a row
	- Insertions and deletions may be made anywhere
	- May represent movie and music collections, grocery store lists, etc.
- **Stacks** are restricted lists
	- Insertions and deletions may be made at one end only
		- These are Last In, First Out (LIFO) structures
	- May be used with compilers and operating systems, and many more applications
- **Queues** are also restricted lists
	- Insertions are made at the back of the queue and deletions are made from the front
		- These are First In, First Out (FIFO) structures
	- May represent waiting lines, etc.
- **Binary Search Trees (BSTs)** require linked data items
	- Efficient for searching and sorting of data
	- May represent directories on a file system, etc.

### What do these C Dynamic Structures have in Common?

- Grow and shrink at runtime
- Implemented with pointers (see [[Modular Programming]])
- Require the use of structs
	- Self-referential structures for linked implementations (see below)

### Self-Referential Structure

- **Self-referential structure**: struct which contains a pointer field that represents the address of a struct of the same type

```
typedef struct node
{
	char data;
	// self-referential
	struct node *pNext;
} Node;
```

### Dynamic Memory Allocation/De-allocation in C

- The growing and shrinking properties may be achieved through functions located in `<stdlib.h>` including:
	- `malloc()` for allocating/growing memory
	- `free()` for de-allocating/shrinking memory
	- `realloc()` for resizing memory
	- Also consider `calloc()`

##### How to use

Assume `Node *pItem = NULL;`

- How to use `malloc()`
	- `pItem = (Node *) malloc (sizeof (Node));`
	- Recall malloc() returns a void \*, which should be type-casted
- How to use `free()`
	- `free(pItem);`
	- Requires the pointer to the memory to be de-allocated
- How to use `realloc()`
	- `pItem = realloc(pItem, sizeof (Node) * 2);`
	- Allocates space for two Nodes and returns pointer to beginning of resized memory