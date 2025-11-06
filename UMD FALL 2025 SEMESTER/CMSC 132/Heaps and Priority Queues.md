---
tags: CMSC_132
created: 2025-11-5
description: 10/31, 11/5 notes (Lecture 25, 27)
---

### Perfect and Complete Binary Trees

A *perfect* binary tree of height $h$ has exactly $2^{(h + 1)} - 1$ elements.

A *complete* binary tree of height $h$ is a perfect tree up to level $h - 1$, in which the leaves at level $h$ are as far left as possible.

### Heaps

A **heap** is a binary tree with two properties:
- It's complete
- Every element (other than the root) is greater than or equal to the value of its parent (a *min heap*)

### Heap Properties

- A heap is a balanced binary tree, so its height is $O(\log(n))$
- The smallest element of a min heap can always be found easily
- The main heap operations are `insert(X)` and `getSmallest()`
- A heap could instead be organized to be able to find the maximum value easily (a *max heap*) if every element (other than the root) is less than or equal to its parent.

### Heap Operation - `insert(X)`

Algorithm:
- Add `X` to end of heap
- While `X` is less than the parent's value, swap `X` with parent (so `X` bubbles up the tree)

### Heap Operation - `getSmallest()`

Algorithm:
- Get the smallest value (at the root)
- Replace the root with `X` at the end of the heap
- While `X` is greater than either child's value, swap `X` with the smaller child
- Return the smallest value (original root)

### Array Heap Implementation

A heap can be easily implemented using an array.

It's a compact representation because the references are implicit (so no memory is required for them).

This works well for complete trees as there's no wasted space.

The locations/indices of elements can be determined using simple formulas based on their relationships:
- Parent of $i$: $\lfloor (i - 1) / 2 \rfloor$
- Left child of $i$: $2i + 1$
- Right child of $i$: $2i + 2$

### Heap Application - Priority Queues

A **priority queue** is a queue whose elements have priority values, so the element with the highest priority is removed first.

A priority queue can be implemented as a heap:
- Enqueue for the priority queue can be implemented using the heap's `insert()`
- Dequeue can be implemented using the heap's `getSmallest()`

### Priority Queue Implementation

- Properties
	- Lower value = higher priority
	- A min heap keeps highest priority items in front
- Another way to implement it is a sorted linked list or array