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

### How do we know which values and operations are supported?

- Each data structure has a corresponding model represented by the abstract data type (ADT)
	- The model defines the behavior of operations, but now how they should be implemented
- **Abstract data types (ADTs)**: a set of data values and associated operations that are precisely specified independent of any particular implementation
- **Data structures**: an organization of information, usually in memory, for better algorithm efficiency, such as a queue, stack, linked list, heap, dictionary, and tree, or conceptual unity, such as the name and address of a person. It may include redundant information, such as length of the list or number of nodes in a subtree.

### ADTs vs. Data Structures

- Many people think that ADTs and data structures are interchangeable in meaning
	- ADTs are logical descriptions or specifications of data and operations
		- To abstract is to leave out concrete details
	- Data structures are the actual representations of data and operations, i.e. implementation
- Semantic vs. syntactic

### Specification of ADT

- Consist of at least 5 items
	- Types/data
	- Functions/methods/operations
	- Axioms
	- Preconditions
	- Postconditions
	- Others?

### Example specification of List ADT

- Description: A list is a finite sequence of nodes, where each node may be only accessed sequentially, starting from the first node
- Types/data
	- "e" is the element type
	- "L" is the list type
- Functions/methods/operations
	- `initList(L)`: procedure to initialize the list L to empty
	- `destroyList(L)`: procedure to make an existing list L empty
	- `listIsEmpty(L) -> b`: Boolean function to return TRUE if L is empty
	- `listIsFull(L) -> b`: Boolean function to return TRUE if L is full
	- `curIsEmpty(L) -> b`: Boolean function to return TRUE if the current position in L is empty
	- `toFirst(L)`: procedure to make the current node the first node in L; if the list is empty, the current position remains empty
	- `atFirst(L) -> b`: Boolean function to return TRUE if the current node is the first node in the list or if the list and the current position are both empty
	- `atEnd(L) -> b`: Boolean function to return TRUE if the current node is the last node in the list or if the list and the current position are both empty
	- `advance(L)`: procedure to make the current position indicate the next node in L; if the current node is the last node the current position becomes empty
	- `insert(L, e)`: procedure to insert a node with information e before the current position or, in case L was empty, as the only node in L; the new node becomes the current node
	- `insertAfter(L, e)`:  procedure to insert a node with information e into L after the current node without changing the current position; in case L is empty, make a node containing e the only node in L and the current node
	- `insertFront(L, e)`: procedure to insert a node with information e into L as the first node in the list; in case L is empty, make a node containing e the only node in L and the current node
	- `insertInOrder(L, e)`: procedure to insert a node with information e into L as node in the list, order of the elements is preserved; in case L is empty, make a node containing e the only node in L and the current node
	- `delete(L)`: procedure to delete the current node in L and to have the current position indicate the next node; if the current node is the last node the current position becomes empty
	- `storeInfo(L, e)`: procedure to update the information portion of the current node to contain e; assume the current position is nonempty
	- `retrieveInfo(L) -> e`: function to return the information in the current node; assume the current position is nonempty
- Axioms
	- Empty()?
	- Not empty()?
	- Others?
- Preconditions
	- Delete() requires that the list is not empty()
- Postconditions
	- After insert() is executed the list is not empty()
- Others?