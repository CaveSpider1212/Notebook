---
tags: CPT_S_121
created: 2024-09-23
description: Lesson 6.1 - Loops
---

### How and When to Use Loops

- If any steps are repeated in a program, use loops
	- If you know in advance how many times it will be repeated, use a counting loop
	- If you don't know, then use a conditional loop

- Kinds of loops
	- Counting loop (`for` or `while`): executes a fixed number of times
	- Sentinel-controlled or Endfile-controlled (`for` or `while`): process data until a special value is encountered
	- Input validation loop (`do-while`): repeatedly accepts interactive input until a value within a specified range is entered
	- General conditional loop (`while` or `for`): repeatedly processes data until a desired condition is met

### Counter Loops

##### while Loops

```
while (<repetition-condition>)
{
	<body>
}
```

- `<repetition-condition>` is evaluated at the beginning of the execution, and if it's true, it runs the `<body>`
- Goes back to the `<repetition-condition>` once the body is done executing, and evaluates again until the condition is no longer true

###### do-while Loops

```
do
{
	<body>
} while (<repetition-condition>);
```

- Similar to while loops, but the program executes the `<body>` first before evaluating the `<repetition-condition>`, so the body is guaranteed to run at least once

##### for Loops

```
for (<initialization>; <repetition-condition>; <update-expression>)
{
	<body>
}
```

- `<initialization>` creates the loop control variable, and it evaluates the `<repetition-condition>` using that variable
- If the `<repetition-condition>` is true, then the program runs the `<body>`
- After the body is done executing, program goes back to the header and updates the loop control variable based on what the `<update-expression>` is
- Keeps evaluating until `<repetition-condition>` is false

### Compound Assignment Operators

```
// the below 2 lines do the same thing
count = count + 1;
count += 1;

// can also be done with -, *, /, and % operators
```

```
count++; // same thing as count += 1
count--: // same thing as count -= 1
```

- **Pre-increment** or **Pre-decrement**: value of the expression is the value of the variable *after* the increment or decrement is applied (so if we were to print this, it would increment/decrement first then print out the new value)
	- `++count` or `--count`
- **Post-increment** or **Post-decrement**: value of the expression is the value of the variable *before* the increment or decrement is applied (so if we were to print this, it would print out the value first, and then increment/decrement it)
	- `count++` or `count--`