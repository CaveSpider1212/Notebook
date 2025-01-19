---
tags: CPT_S_121
created: 2024-11-15
description: Lesson 13.2
---

- **Dynamic data structures**: structures that expand and contract as a program executes
	- Memory allocated as needed (dynamically)
	- Can use dynamic memory allocation to dynamically allocate an array at runtime, so we don't need to constrain the maximum size of an array at compile time
	- Memory can be allocated to store any of the simple or structure data types (like structs, ints, doubles, etc.)
	- Separately allocated structured blocks are called *nodes*, which can be used to form composite structures that expand and contract while the program executes

### Review of Pointers

(see [[Modular Programming]])

See the example below:
```
int num = 3; // this has an address of 1000
int *nump = &num; // this has an address of 2000
```

References:
- Direct value of *num* is 3 (this is directly stored in num)
- Direct value of *nump* is 1000 (this is the address of the *num* variable, where *nump* is pointing to)
- Indirect value of *nump* (\*nump) is 3 (this is the value of *num*, which *nump* can access as an indirect value by pointing to the address of *num*)
- The address of *nump* (&nump) is 2000

### `malloc` Function

^556d39

(found in `<stdlib.h>`)

`void *malloc(size_t size); // function prototype` ^75a6c8

- The argument in the function prototype above indicates the amount of memory space needed to be allocated
	- We can use the `sizeof` operator to determine this number
- For example, `malloc (sizeof (int))` allocates exactly enough space to hold one integer
- A call to `malloc` returns a pointer to the block of memory allocated (NULL if no memory can be allocated)
- We need to assign the pointer to a specific pointer type using type casting since the return type of `malloc()` is void

```
int *nump = (int *) malloc (sizeof (int));
```

- **Heap**: area in which the dynamic memory is allocated
- **Stack**: area that stores function data when functions are entered
	- The stack goes away when the function is exited

### `calloc` Function

^5ac23e

(found in `<stdlib.h>`)

`void *calloc (size_t nitems, size_t size); // function prototype`

- Used to allocate contiguous blocks of memory for array elements
- The 2 arguments are the number of array elements needed and the size of one element (see prototype above)
- Returns a `void *` to the beginning of the allocated blocks of memory, like `malloc`, so we must use explicit type casting with the pointer type

```
Point array[10]; // static allocation
Point *struct_ptr = (Point *) calloc (10, sizeof(Point)); // dynamic allocation

// the two lines above do similar things, but how they are allocated is different
```

- Elements in array can be accessed using array notation as usual

### Freeing Allocated Memory

^2b3cd9

- Use the function `free(pointer)` to return the allocated memory pointed to by the pointer to the heap
- Not freeing memory can lead to "memory leaks," which are a common source of run-time program bugs and slowing down a program's execution