---
tags: CPT_S_121
description: Lesson 1.2 - C Language Elements
created: 2024-08-28
---

### About C

- Best for operating systems and low-level programming
- Also works well as a general-purpose programming language
- Many computers support C as they have a C compiler
- Works cross-platform

### Elements

- Comments
  - `//` creates single-line comments
  - `/* */` creates block comments (can span multiple lines)
- **Preprocessor directives**: tell the preprocessor (program that modifies the C file before compiling) to modify the program before compilation
  - Begins with `#` with no semicolon at the end
  - Use `#include` to use a library by including it in the header file
    - Libraries are needed to run specific functions needed for some tasks or operations
  - Use `#define` to replace each occurrence of a textual constant (like PI) with a value (3.14159)
- `main` method: required in all C files, contains all of the executable statements, "drives" the rest of the program

#### Reserved Words

- Lowercase
- Have special meaning (like int, double, etc.)

#### Standard Identifiers

- Represent names of operations (like `printf` and `scanf`)
- Can be redefined, but not recommended

#### User-Defined Identifiers

- Variables and functions
- Conditions
  - Must contain of only letters, numbers, or underscores
  - Must not begin with digits
  - Must not conflict with reserved words
  - Should not redefine standard C library identifiers

#### Variable Declarations

- Reserves memory space for a value
- Also associates the memory cell with a name (user-defined identifier)

### Data Types

- **Data type**: range of values that can be represented in memory, and can have operations performed on those values

##### int

- Integers (-32767 to 32767, but most machines define 32-bit integers)
- Operators
  - **Math**: +, -, \*, /, %
  - **Comparison**: >, <, <=, >=, \=\=, !=
- `%xd`: format for an integer using *x* number of columns
	- If *x* is greater than the length of the integer, then it shows blank spaces to the left of the integer
	- If *x* is less than or equal to the length of the integer, then the integer is displayed normally (no blank spaces next to it)

##### double

- Models real numbers (must include decimal point), but not all real numbers can be modeled due to space limitations (64-bit)
- Same operations defined for doubles as with integers
- Scientific notation can be used to write doubles (using 'e')
- `%x.yf`: format for a double or float using *x* number of columns and *y* number of decimal places
	- If *x* is greater than the length of the double, then it shows blank spaces to the left of the integer
	- If *x* is less than or equal to the length of the double, then the double is displayed normally (no blank spaces next to it)
	- If *y* is greater than the number of decimal places already in the double, then extra 0's are added to the end of the double
	- If *y* is less than the number of decimal places already in the double, then the double is shortened to *y* number of decimal places and rounded up or down

##### char

- Models individual ASCII characters (8-bit)
- Able to use comparison operations
- Use single quotes for defining char variables
- `%c`: format for a character