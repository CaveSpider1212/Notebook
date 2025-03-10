---
tags: CPT_S_122
created: 2025-2-24
description: Lesson 7.1
---

### What is Operator Overloading?

- A generalizing of function overloading
- **Operator overloading**: an extension to C++ standard operators to define how they should work with user-defined types such as classes

### Why Overload Operators?

- Improves readability
- Allows for a more natural way to implement code

### Rules and Restrictions on Operator Overloading

- The precedence of an operator cannot be changed
- The associativity of an operator cannot be changed, i.e. left-to-right or right-to-left
- The "arity" of an operator cannot be changed, i.e. if the operator accepts one operand (unary) or two operands (binary)
- Only existing operators may be overloaded

### Which Operators Cannot be Overloaded?

- .
- .* (pointer to member)
- ::
- ?:

### Why Non-Member Overloaded Operators?

- Enables "symmetry" among operators