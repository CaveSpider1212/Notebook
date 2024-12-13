---
tags: CPT_S_121
created: 2024-09-16
description: Lesson 4.2 - Selection Structures in C
---

### Conditions

- Rely on a Boolean condition, which can be true (1) or false (0)
- Relational operators (<, >, <=, >=, \=\=, !=) used for Boolean conditions
- Relational operators combined using logical operators (&&, ||, !)
- Operator precedence order (top to bottom)
	- !, +, -, and unary operators
	- \*, /, %
	- +, -
	- <, <=, >=, >
	- \=\=, !=
	- &&
	- ||
	- =
- **Short-circuit evaluation**: program stops evaluating AND statement if the first part is false, and an OR statement if the first part is true
- **De Morgan's laws**: used to complement compound logical expressions (make every relational operator the opposite, and switch the AND and OR operators as well)

### If-statements

```
if (condition) {
	body
}
```

- Does the body if the condition is true

```
if (condition) {
	body if true
}
else {
	body if false
}
```

- Does the first body if the condition is true, otherwise does the second body

### Switch Statements

- More readable, faster, and easier to debug than if statements

```
switch (variable) {
	case value1:
		// do action if variable == value1
		break;
	case value2:
		// do action if variable == value2
		break;
	case value3:
		// do action if variable == value3
		break;
	default:
		// do action if variable is anything other than value1, value2, or value3
		break;
}
```

- The "variable" in the switch statement cannot be a string or double
- Must use "break", otherwise the switch statement will just go to the next case label without stopping there
- Good idea to add a default case