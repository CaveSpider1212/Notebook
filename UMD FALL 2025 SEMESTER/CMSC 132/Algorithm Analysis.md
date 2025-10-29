---
tags: CMSC_132
created: 2025-10-21
description: Video lecture (Slides part of Lecture 23)
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
