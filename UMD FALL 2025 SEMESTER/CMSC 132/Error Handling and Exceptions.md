---
tags: CMSC_132
created: 2025-9-19
description: 9/17, 9/19 notes
---

### Tests

If we have tests, and our code fails some tests, the first thing we should immediately do is write more tests to improve the coverage. There are 3 types of coverage (line/statement, branch, and path).

> [!info] Line/Statement Coverage
> Measures what percentage of the lines/statements of some code were executed by a set of tests that were run.
> 
> Looks at whether each line (or statement) of the program was executed at least once in the tests.

> [!info] Branch Coverage
> Measures what percentage of the control points (i.e. conditions) in some code being tested were executed in all possible ways by a set of tests of it (for example if an if statement was tested when it was both true and false).

> [!info] Path Coverage
> Measures what percentage of all the different execution sequences through some code were executed by a set of tests of it (for example, all possible execution sequences of a method must be tested).

### Types of Errors

**Syntax errors** are errors in code construction, which could include typographical, grammatical, or type mismatch problems.

**Runtime errors** are operations that are illegal or impossible to execute and are treated as exceptions in Java.

**Logic errors** are operations leading to an incorrect program state, and they represent a problem in the design or implementation of the algorithm used.

### Handling Errors

One way a method can handle an error is to propagate it back to the caller in some way, which can be done through:
- Returning an error code to the caller
- Using exceptions (and `try`-`catch`-`finally` blocks)
	- `try` attempts to execute whatever is in the block
	- `catch` catches any exceptions thrown by a function
	- `throw` generates an exception and is usually called in some sort of method that the `try` block calls
	- `finally` executes the code in the block regardless of whether there was an exception or not, and is optional to have

> [!tip] `try`-`catch`-`finally` blocks
> ```
> try {
> 	method();
> } catch (ExceptionType e) {
> 	// executes when exception is thrown
> } finally {
> 	// executes anyways
> }
> 
> void method() {
> 	if (condition) {
> 		throw new ExceptionType();
> 	}
> }
> ```
> 
> If an exception were to occur in a `try` block:
> 1. Execution leaves the try block and jumps straight to the first `catch` block associated with the `try` block whose exception matches the type that was thrown (either same type or a supertype), meaning nothing below the point where the exception occurred is executed.
> 2. If there's a matching `catch` block, its code is executed.
> 	1. If there is no matching `catch` block, the execution returns from the method that's running and the same procedure occurs in the method that called it until a matching `catch` block is found, and if the execution goes back to the `main()` method then the JVM will terminate the program. 
> 	2. If a `try` block has an associated `finally` block it is executed before transferring control to the caller.
> 3. The `finally` block's code is executed if there is one

### Types of Exceptions

> [!info] Checked Exceptions
> **Checked exception**: checked at compile time, and these are the ones we explicitly throw and catch and use try-catch blocks with
> 
> The "catch-or-declare" policy for checked exceptions means that if a method's code were to throw an exception, it must either be handled locally with a `catch` block or the method must have `throws` in the signature, which forces the method calling it to handle it themselves using this policy.

> [!info] Unchecked Exceptions
> **Unchecked exception**: checked at runtime, and not required to be thrown and caught/use try-catch blocks with them (JVM will handle it instead).
> 
> The classes `RuntimeException` and `Error` and their descendant classes are unchecked exceptions, which include `NullPointerException` and `IndexOutOfBoundsException`

### Designing and Using Exceptions

Place statements that jointly accomplish a task into a single `try` block.

Use existing Java library exceptions (when throwing/catching) if possible.

Avoid simply catching and ignoring exceptions (i.e. put something in a catch block).

Use exceptions only for rare, incorrect, unexpected events (i.e. to handle errors), not for expected processing tasks like checking for loop termination, end of an array, or testing for null.

Advantage of using exceptions:
- Clear separation between normal program logic and error-handling logic
- Exceptions can be organized into hierarchies using inheritance, allowing for specific handling of different types of errors
- Improves readability