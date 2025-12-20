---
tags: CMSC_132
created: 2025-10-21
description: 10/17, 10/20 notes (Lectures 19 and 20)
---

### Stacks

A **stack** is a restricted list where elements can only be accessed or removed from one end, and only added at the same end.

This means elements are removed in the *opposite* order of insertion, resulting in LIFO (last-in, first-out) behavior.

Operations:
- Push: Add element (to the top)
- Pop: Remove element (from the top)
- Peek/Top: Return the current top element, without removing it
- IsEmpty: Return true if a stack has no elements, false otherwise

Applications:
- Converting arithmetic expressions to postfix
- Solving postfix expressions
- Checking for matching parentheses or symbols like HTML tags
- Runtime stack

Implementations:
- Linked: Add elements to and remove elements from one end of a list (the same end)
- Array: Increment and decrement an index for push and pop operations

### Queues

A **queue** is a restricted list where elements can only be accessed or removed from one end, and only added at the opposite end.

This means elements are removed *in order* of insertion, resulting in FIFO (first-in, first-out) behavior.

Operations:
- Enqueue: Add an element to the back of a queue
- Dequeue: Remove an element from the front of a queue (usually returns it also)
- IsEmpty: Returns true if a queue has no elements, false otherwise

Applications:
- Songs to be played
- Jobs to be printed
- Customers to be served

A **deque** is a double-ended queue, so elements can be added, accessed, or removed at either end.

Implementations:
- Linked: Add elements to the tail (back) of a list, and remove elements from the head (front) of the list
- Array: Need to use a "circular" array where `q[0]` follows `q[capacity - 1]`, and increment the front position by saying `front = (front + 1) % capacity` each time an element is deleted