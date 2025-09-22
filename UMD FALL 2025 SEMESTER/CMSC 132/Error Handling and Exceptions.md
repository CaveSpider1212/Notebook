---
tags: CMSC_132
created: 2025-9-19
description: 9/17, 9/19 notes
---

If we have tests, and our code fails some tests, the first thing we should immediately do is write more tests.

One way a method can handle an error is to propagate it back to the caller in some way, which can be done through:
- Returning an error code to the caller
- Using exceptions (and try-catch-finally blocks)

### Designing and Using Exceptions

Place statements that jointly accomplish a task into a single try block.

Use existing Java library exceptions (when throwing/catching) if possible.

Avoid simply catching and ignoring exceptions (i.e. put something in a catch block).

Use exceptions only for rare, incorrect, unexpected events (i.e. to handle errors), not for expected processing tasks like checking for loop termination, end of an array, or testing for null.

Advantage of using exceptions:
- Clear separation between normal program logic and error-handling logic
- Exceptions can be organized into hierarchies using inheritance, allowing for specific handling of different types of errors
- Improves readability
- 