---
tags: CPT_S_121
created: 2024-11-6
description: Lesson 12.1 & 12.2
---

**Recursion**: process in which a function calls itself either directly or indirectly through another function

```
int recursiveFunction(int r, int s)
{
	recursiveFunction(r, s - 1);
}
```

### Nature of Recursion

- Problems that may be solved using recursion have these attributes
	- One or more simple cases have a straightforward, non-recursive solution
	- The other cases may be defined in terms of problems that are closer to the simple cases
	- Through a series of calls to the recursive function, the problem eventually is stated in terms of the simple cases
- Things about recursion
	- Divide and conquer approach
	- A fresh copy of a function goes to work on a similar, but simpler problem than the original
	- Alternative to iteration

### Properties of Recursion

- Recursive solutions have at least two cases:
	- **Simple/base case**: ends the recursion
	- **Recursive cases/steps**: calls the function again and keeps the recursion going

```
int multiply(int m, int n)
{
	int ans;

	if (n == 1)
	{
		ans = m; // this is the base case
	}
	else
	{
		ans = m + multiply(m, n - 1); // this is the recursive step
	}

	return ans;
}
```

### Advantages/Disadvantages

##### Advantages of Recursion

- May provide a simpler solution than an iterative one
	- Sometimes iterative solutions lend themselves to complex algorithms
- May lead to reduction in code size
- May lead to reduction time complexity

##### Disadvantages of Recursion

- May require large amounts of memory
	- For each call to the function more memory is allocated for local variables
	- "Call stack" continues to grow for each call; may lead to stack overflow
		- Recall the call stack keeps track of a point to which each active function or subroutine should return control when finished
- Difficult to test and debug