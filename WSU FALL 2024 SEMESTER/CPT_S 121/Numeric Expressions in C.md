---
tags: CPT_S_121
description: Lesson 2.1 - Numeric Expressions in C
created: 2024-08-30
---

### Mixed-Type Expressions

- If the types of operands in the expression are different (like an integer and a double), the result is always a more precise result (in this case a double)
  - Think of it like boxes...int has a smaller box and double has a larger box, the result won't fit in the "integer" box but will fit in the "double" box so it goes there

- Expressions are evaluated from right-to-left
  - The expression is evaluated first, then the result is assigned to the variable

##### Type Casting

- Implicit casting
```
int num1 = 12;
double num2;
num2 = num1 // num1 is implicitly casted to a double, and num2 becomes 12.0
```

- Explicit casting
```
double num1;
num1 = (double) 1 / 5; // 1 is explicitly cast to a double, making it 1.0; answer is 1.0 / 5 = 0.2
```

### Operators

- **Unary operators**: consist of one operand (like a negative symbol)
- **Binary operators**: consist of two operands (like +, -, /, etc.)

##### Operator Precedence

> [!info] Rules
> - Evaluation from left to right of the expression
> - Subexpressions in parentheses are evaluated first
> - If no parentheses are used, \*, /, and % take precedence over + and -

- Unary operators take precedence over binary operators, and are evaluated from right to left