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