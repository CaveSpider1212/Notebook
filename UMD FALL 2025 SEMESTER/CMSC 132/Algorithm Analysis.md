---
tags: CMSC_132
created: 2025-10-21
description: Video lecture (Slides part of Lectures 23 and 24), 12/10, 12/12 notes (Lecture 40, 41)
---

**Efficiency** has to do with how many resources are used by an algorithm, and two ways to measure it are benchmarking and asymptotic analysis.

### Benchmarking

- Approach:
	- Code the algorithm up as a program
	- Run the program on some inputs (often on well-known standard inputs)
	- Measure the time and memory space it uses (often compare them against other known results for those inputs)
- Advantage:
	- Gives precise information for a given configuration (implementation, hardware, inputs)
- Drawbacks:
	- Is affected by the specific configuration
	- Is affected by special cases (biased inputs)
	- Does not measure intrinsic efficiency

### Asymptotic Analysis

- Approach: Analyze an algorithms efficiency mathematically, and express its running time *not* in units of time, but *instead* as a function of the input size (which is called `n`)
	- Running time is `O(f(n)`, meaning time is called on the order of some function `f(n)` (called "big O" notation)
- Advantages:
	- Measures intrinsic efficiency
	- The programming language, compiler, and hardware are irrelevant

### Upper Bound

Big-O represents an *upper bound* on the number of operations performed by an algorithm, for a sufficiently large input size--the intrinsic efficiency of the algorithm for large inputs

### Formal Definition of Big-O

A function $T(n))$ is $O(f(n)$ (where $f(n)$ is some other function) if, for some integer constants $c > 0$ and $n_0 \geq 1$, $T(n) \leq c \times f(n)$ everywhere that $n \geq n_0$
- In other words, you can identify a coefficient $c$ and an input value $n_0$ with the properties that, for all input sizes that are greater than or equal to $n_0$, $T(n)$ is always smaller than $c \times f(n)$

### Common complexity categories

From smallest to largest, for input problem size $n$ and constant $k > 1$:
> |Complexity|Name|Examples
> |-|-|-
> |$O(1)$|Constant|Add element to front of linked list
> |$O(\log(n))$|Logarithmic|Binary search
> |$O(n)$|Linear|Max of unordered list/array
> |$O(n \log(n))$|$n \log n$|
> |$O(n^2)$|Quadratic|2D matrix addition
> |$O(n^3)$|Cubic|2D matrix multiplication
> |$O(n^k)$|Polynomial|
> |$O(k^n)$|Exponential|
> |$O(n!)$|Factorial|
> |$O(n^n)$|$n$ to the $n$|

### Determining asymptotic complexity

As $n$ increases, the highest-order term of a function (that represents the running time of an algorithm, in terms of the input size $n$) dominates its value. Lower order terms, and the highest order term's coefficient, can be ignored.

For example, if $T(n) = \frac{1}{2} n \log(n) + 10n$, then it is $O(n \log(n))$.

### Analyzing Algorithms

We would like to be able to determine the asymptotic complexity of an algorithm.

Approach:
- Ignore the less frequently executed parts of the algorithm
- Find the **critical section** of the algorithm
- Determine how many times the critical section is executed as a function of the input problem size $n$

##### Critical section of algorithm

The execution time of an algorithm's critical section is what dominates its overall execution time.

Characteristics
- It's the operation central to the functioning of the algorithm
- It's contained inside the most deeply nested loops (or recursive calls)
- It's executed as often as any other part of the algorithm

> [!tip] Algorithm Time Function Tips
> If multiplying $n$ $k$ times is involved, then generally that loop/sub-loop runs $n^k$ times.
> 
> If addition or subtraction by $k$ is involved, then generally that loop or sub-loop runs $\frac{n}{k}$ times.
> 
> If multiplying or dividing $n$ by $k$ each iteration is involved, then generally that loop/sub-loop runs $\log_k(n)$ times.

### Best Case and Worst Case

- The **best case** is the smallest number of operations required
- The **worst case** is the largest number of operations required
- The **average case** is the number of operations required for the "typical" case

### Efficiency of Searching an Array or List

- Sequential (linear) search
	- Array: $O(n)$
	- Linked: $O(n)$
	- No difference if the array/linked list is ordered/sorted or not
- Binary search: $O(\log n)$
	- Requires the list/array to be ordered
	- Can be performed with an ordered linked list, but it is impractical since we can't find the middle element by the index

> [!info] Efficiency of array operations:
> 
> |Operation|Unsorted array|Sorted array
> |-|-|-
> |Lookup (search) and insertion|$n + 1 = O(n)$|$\log(n) + n = O(n)$
> |Insertion only (without lookup)|$O(1)$|$O(n)$
> |Lookup (search) and deletion|$n + 1 = O(n)$|$\log(n) + n = O(n)$
> |Deletion only|$O(1)$|$O(n)$
> |Indexing|$O(1)$|$O(1)$

> [!info] Efficiency of linked list operations:
> 
> |Operation|Unordered linked list
> |-|-
> |Lookup (search) and insertion|$n + 1 = O(n)$
> |Insertion only|$O(1)$
> |Lookup (search) and deletion|$n + 1 = O(n)$
> |Deletion only|$O(1)$
> |Indexing|$O(n)$
> 
> It does not make a difference in the algorithm efficiency if the list is ordered or not.

### Patterns Useful for Time Complexity Analysis

$$1 + 2 + 3 + ... + n = \frac{n (n + 1)}{2}$$
$$(n - 1) + (n - 2) + (n - 3) + ... + 1 = \frac{n (n - 1)}{2}$$
$$1 + 2 + 4 + 8 + ... + n \approx 2n$$

### Additional complexity measures

- Big-O ($O(...)$) is an upper bound on the amount of work.
	- For example, $3n^2 + 6n - 2$ is $O(n^2)$, but it's also $O(n^3)$, $O(2^n)$, $O(n!)$, etc.
	- $3n^2 + 6n - 2$ isn't big-$O$ of anything smaller than $O(n^2)$, so that is its big-O notation
- Big-Omega ($\Omega (...)$) is a lower bound on the amount of work
	- For example, $3n^2 + 6n - 2$ is $\Omega(n^2)$, but it's also $\Omega(n)$, $\Omega(\log n)$, $\Omega(1)$, etc.
	- $3n^2 + 6n - 2$ is not big-$\Omega$ of anything larger than $\Omega(n^2)$, so that is its big-Omega
- Big-Theta ($\Theta(...)$) is a combined bound on the amount of work -- it represents the closest possible (tight or exact) bound
	- $3n^2 + 6n - 2$ is $\Theta(n^2)$, because it's $O(n^2)$ and it's also $\Omega(n^2)$
	- $3n^2 + 6n - 2$ is only $\Theta(n^2)$, not of any other function

### Other important complexity categories

- Categories
	- P: Deterministic polynomial time
	- Exponential: Requires exponential time
	- Decidable: Can be solved by an algorithm
	- Undecidable: Not solvable
	- NP: Nondeterministic polynomial time

If a problem has an algorithm that solves it in time X, then the problem is said to be in X.

### Some NP problems

- Traveling salesperson (TSP)
- Knapsack problem
- Boolean satisfiability

All have no known polynomial time general solution (but a possible solution to any of them can be checked or verified, meaning to see if it's correct, in polynomial time).

### What if a problem is not in P?

The fact that a problem can't be solved in polynomial time means that no algorithm or program can solve *all* cases of it *exactly*, in a *reasonable* amount of time, but there might be an algorithm that always runs quickly and gives close approximations or quickly gives exact answers.

### Algorithm strategies

- Problem type
	- Satisfying: Find any working solution to the problem
	- Optimization: Find the best solution

> [!info] Recursive algorithms
> This approach is based on reapplying an algorithm to its subproblems.

> [!info] Backtracking algorithms
> This approach is based on recursive depth-first search.
> 
> Approach:
> - Test whether a solution has been found; if so, return it
> - Otherwise for each choice that can be made:
> 	- Recurse on that choice
> 	- If the recursion returns a solution, return it
> - If no choices remain, return failure

> [!info] Divide and conquer algorithms
> This approach is based on dividing a problem into subproblems.
> 
> Approach:
> - Divide a problem into smaller subproblems
> 	- The subproblems must be of the same type
> 	- The subproblems do not need to overlap
> - Solve each subproblem (usually recursively)
> - Combine the subproblems' solutions to solve the original problem
> 
> Used in merge sort or quick sort

> [!info] Dynamic programming algorithms
> This approach is based on remembering past results, to avoid having to recompute them.
> 
> Approach:
> - Divide a problem into smaller subproblems
> 	- The subproblems must be of the same type
> 	- The subproblems *must* overlap
> - Solve each subproblem recursively
> 	- This may simply look up the solution (if it was previously solved)
> - Combine the subproblems' solutions to solve the original problem
> - Store the solution if not already solved
> 
> Generally applied to optimization problems (Dijkstra's algorithm is an example)

> [!info] Greedy algorithms
> This approach is based on trying the best current (local) choice whenever an algorithm has multiple options it can select from
> 
> Approach:
> - At each step of the algorithm choose the best local option
> 
> Avoid backtracking and exponential time ($O(2^n)$).
> 
> Sometimes choosing a local optimum leads to the global optimum (but sometimes not).
> 
> Somewhat used in Dijkstra's algorithm

> [!info] Brute-force algorithm
> This approach is based on trying all possible solutions.
> 
> Approach:
> - Generate and evaluate all possible solutions until:
> 	- A satisfactory solution is found
> 	- The best solution is found (if can be determined)
> 	- All possible solutions are found, returning the best one
> 	- Return failure if no satisfactory solution (or no solution) was found
> 
> Generally the most expensive approach ($O(n!)$ complexity).

> [!info] Branch and bound algorithms
> This approach is based on limiting search using current best solution.
> 
> Approach:
> - Keep track of the best solution seen so far
> - Eliminate (*prune*) partial solutions that can't improve upon the best solution seen so far
> 
> Reduces the search space, but is not guaranteed to avoid exponential time ($O(2^n)$)

> [!info] Heuristic algorithm
> This approach is based on trying to guide search for solution.
> 
> A heuristic is a rule of thumb.
> 
> Approach:
> - Generate and evaluate possible solutions using rule of thumb
> - Stop if a satisfactory solution is found
> 
> This can reduce complexity but is not guaranteed to yield the best solution