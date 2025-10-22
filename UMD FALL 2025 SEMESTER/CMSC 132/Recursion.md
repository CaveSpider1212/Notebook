---
tags: CMSC_132
created: 2025-10-8
description: 10/8, 10/10 notes
---

### What is Recursion?

- **Recursion**: Solving problems where a method calls itself
- Base case: condition where the recursion ends (need to have some sort of conditional statement, like an `if` statement, to identify base case)
	- If a problem instance is simple or trivial, just solve it directly
- Recursive step: where the function is called again
	- Simplify the problem instance into smaller instances of the same problem
	- Solve the smaller instances using the same algorithm
	- Combine the solutions to the smaller instances in a way that solves the original problem

### Properties of Recursion

- Recursion relies on the runtime call stack (each method call gets its own stack space)
- Any problem that can be solved with iteration can be solved with recursion, and vice versa (but one way may be better than the other for some problems)

### Making Recursion Work

In designing a correct recursive method you need to ensure that:
- The base cases are recognized correctly and solved correctly
- The recursive cases solve one or more simpler subproblems
- The solution to the overall problem are correctly being calculated from the solutions to the simpler subproblems

### Forms of Recursion

**Tail recursion**: The recursive call is the very last thing performed in the recursive step

**Non-tail recursion**: The recursive call is not the last thing performed in the recursive step

### Recursion vs. Iteration

Iterative algorithms are usually more efficient, as there is some overhead for recursive method calls

Recursive methods:
- Have higher overhead (time to perform method calls as well as memory for the runtime call stack)
- May be simpler, so easier to write, understand, debug, and maintain
- Are natural for backtracking searches
- Well suited for self-referential data structures

Possible problems with recursion:
- Incorrect recursive calls (leading to a function calling itself "infinitely")
- Inefficiency (excessive computations/method calls may happen)

### Binary Search

- Set low and high to be the lowest and highest indices of the array
- Check if the middle value (halfway between low and high) is the one being searched for
- If the middle value is larger than the element being searched for, set high to middle - 1
- If it's smaller, then set low to middle + 1
- Repeat until the number has been found or the array range remaining to be searched in is empty