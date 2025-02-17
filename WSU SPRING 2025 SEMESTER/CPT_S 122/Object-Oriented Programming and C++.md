---
tags: CPT_S_122
created: 2025-2-10
description: Lesson 5.1
---

### Object-Oriented Design

- Model software in ways that are similar to how people view/describe real-world objects
- Descriptions and designs include properties or attributes of the real-world objects
- The Unified Modeling Language (UML) provides a specification for illustrating properties of objects along with interactions between them

### Object-Oriented Programming

- Programming language model which institutes mechanisms to support implementing object driven software systems
	- C++, C#, Java
- Procedural programming, such as instituted by C, is action oriented
- In C, the unit of programming is a function
- In C++ the unit is a `class`

### Classes and Objects

- **Class**: user-defined type or data structure, containing data members (attributes) and member functions (operations)
	- Blueprint for an object
- **Object**: instantiation of a class
	- Class is the type, object is the variable with allocated memory for that type

### Data Encapsulation

- **Encapsulation**: a way of organizing or wrapping of data/attributes and methods/operations into a structure (or capsule)
	- Demonstrated by objects
	- Objects naturally impose encapsulation, as attributes and operations are closely tied together

### Abstraction/Information Hiding

- **Abstraction**: a design principle which states a design decision should be hidden from the rest of the system
	- Objects should communicate with each other through well-defined interfaces, but not know how other objects are implemented
- Prevents access to data aside from the methods specified by the object
- Guarantees integrity of data
- Access specifiers in C++ control the access to information
	- `public`, `protected`, and `private`

### Basics of C++ and I/O

- In C++, just like in C, every program begins execution with `main()`
- to perform input and output (I/O) we need to include the C++ Standard Library `<iostream>`
	- Essentially replaces `<stdio.h>`, but with even more richness and convenience
	- If we say `using std::(operation)` we can just call the operation in the code without saying "`std::`" before
- Use standard output stream object (`std::cout`) and stream insertion operator (`<<`) to display information to the screen
	- Replaces `printf()`
	- Example: `cout << "Enter a number: ";` prints out the string to the screen
- Use standard input stream object (`std::cin`) and stream extraction operator (`>>`) to read data from the keyboard
	- Replaces `scanf()`
	- Example: `cin >> n1;` to read user input into n1

### Reference and Reference Parameters

- There are two ways to pass arguments to function in C++
	- **Pass-by-value (PBV)**: a copy of the contents/value of each argument is made and passed (on the function call stack) to the called function
		- One disadvantage of pass-by-value is copying the contents of a large data item or object introduces longer execution times and memory space
		- In general, should only be used with simple types
		- Passing-by-pointer falls under this category
	- **Pass-by-reference (PBR):** NO copy of the contents/value of each argument is made
		- The called function can access the caller's data directly, and modify the data
- We don't use pass-by-reference strictly so that we can modify the data in an object directly, in many cases we use it so that the overhead of copying data is circumvented
- We use the ampersand (&) to represent pass-by-reference
	- i.e. `void cube (int &n);`
	- Don't confuse with the address of (&) operator....context determines which one's in play
- We can return a reference to a variable
	- i.e. `int & someFunction (int &n);`
	- If we return a reference to an automatic local variable, the variable becomes undefined when the function exits; unless the variable is declared as "static" (keyword)
		- References to undefined variables are called *dangling* references
		- Note: dangling references and dangling pointers are NOT the same

### Unary Scope Resolution Operator

- **Unary Scope Resolution Operator (::)**: allows a global variable to be accessed without confusing it with a local variable

```
int num = 42; // global variable
int main (void)
{
	double num = 100.25; // local variable
	cout << num << endl; // displays 100.25
	cout << ::num << endl; // displays 42
}
```

### Function Overloading

- **Function overloading**: the ability to define multiple functions with the same name
	- Each function must have different types, different numbers, and/or different order of parameters
- The C++ compiler selects the appropriate function based on the *number*, *types*, and *order* of arguments in the function call
- We use function overloading to increase readability and understandability
	- We only want to overload functions that perform similar tasks

### C++ Standard Template Library (STL) Class Vector

- STL class `vector` represents a more robust array with many more capabilities
- May operate with different types of data because they're templated

```
vector<int> v1(10); // declares a 10 element vector of integers

vector<double> v2(5); // declares a 5 element vector of doubles
```