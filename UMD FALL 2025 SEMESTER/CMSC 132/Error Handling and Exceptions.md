---
tags: CMSC_132
created: 2025-9-19
description: 9/17, 9/19 notes
---

If we have tests, and our code fails some tests, the first thing we should immediately do is write more tests.

One way a method can handle an error is to propagate it back to the caller in some way, which can be done through:
- Returning an error code to the caller
- Using exceptions (and try-catch-finally blocks)