---
tags: CPT_S_121
description: Lesson 2.2 - Functions
created: 2024-09-06
---

### Top-Down Design

- **Top-down design**: taking a bigger problem and splitting it into smaller subproblems and solving each subproblem, and combining solutions to solve the big problem
- Good to use structure charts when doing top-down design
	- Contains one big problem, then subdivided into multiple smaller problems (subproblems), then each subproblem contains functions that relate to that particular subproblem

### Functions

- **Functions**: "Mini-programs" that solve a bigger problem; use top-down design
- May have input arguments
- Returns result using the return statement
- Can be reused and tested easily (and even reused across projects)

> [!info]
> `void functionName(parameter)`: This is a **function header**
> 
> - `void` is the **return type** of the function (in this case, doesn't return anything)
> - `parameter` is a **formal parameter** of the function to be passed into the function
> 	- Write `void` in the parameter section if there are no parameters
> 	- **Arguments**: variables/data passed into the function where it is called (for example, in `functionName(args)`, `args` is passed into the function)
> 		- Note: When there isn't a pointer being used, it is a *copy of the value* that is being passed into the function (meaning changing the value in the function doesn't actually change the value of the variable)

### Compiling and Executing Functions

- Functions prototypes tell the compiler what functions are defined, and the program is already aware of the function when it is encountered in the main method
- Each function is compiled after the main function
- When a function is executed, memory space for the local variables in the function are allocated, but is released once the function is done executing
	- That is why local function variables can only be used in the function
	- This is related to the **scope** of a function

### Terms to Know

- **Coupling**: how interdependent the modules or components within the software are (in the case of functions, how interdependent they are in the program)
- **Cohesion**: measure of how focused and related the functionality is within a single unit or code block