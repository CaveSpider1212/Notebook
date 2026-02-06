---
tags: CMSC_216
created: 2026-2-3
description: 2/3, 2/5 notes
---

Every programming language should have:
- Comments
- Statements/expressions
- Variable types
- Assignment
- Function declarations

### Traditional C Data Types

The ranges of values are slightly more negative than positive.

There are no `boolean` or `String` types in C since `booleans` are represented only as 0 = false and everything else = true, and strings are arrays of characters.

> [!info] Integral Data Types
> Bytes|Name|Range
> -|-|-
> 1|`char`|-128 to 127
> 2|`short`|-32,768 to 32,767
> 4|`int`|-2,147,483,648 to 2,147,483,647
> 8|`long`|-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807

> [!info] Floating Data Types
> Bytes|Name|Range
> -|-|-
> 4|`float`|$\pm$ 3.40282347E $\pm$ 38 (6-7 significant decimal digits)
> 8|`double`|$\pm$ 1.79769313486231570E$\pm$ 308 (15 significant decimal digits)

> [!info] Pointer Data Types
> Bytes|Name|Description
> -|-|-
> 4/8|Pointer|Pointer to another memory location
> Size of array $\times$ size of an element|Array|Pointer to a fixed location
> 
> On a 64-bit machine, all pointers are *8 bytes*.

### `void` Pointers

Pointers with a specific data type may only point at variables of that data type and nothing else. If this is violated, then a compile-time error will happen (Type Error).

`void *ptr` declares a pointer to something/anything and is useful to store an arbitrary memory address (meaning it can point to variables of any data type).

It removes the compiler's ability to **type check** so it is dangerous.

It can be casted to a specific pointer type, but only the same type as the variable it is pointing to.

### Arrays

**Arrays** are continuous blocks of homogenous data.

They are automatically allocated by the compiler with a *fixed size*.

The name of the array represents the *memory address where the array starts* (so the first element).

### Pointer/Array Relationship

Arrays:
- Allocated by the compiler at a *fixed location*
- The bare name references the starting address of the array
- Must use square braces \[] to index into them

Pointers:
- Can point to anything, can change, must be manually directed
- Can use either square braces \[] or dereferencing to index into them

Interchangeability:
- In most cases, functions that require an array can have a pointer passed into it, and vice versa
- This works because array variables are passed as their starting memory address, which is a pointer value

### Pointer Arithmetic

Assigning an array name to a pointer sets the pointer value to the address of the first element of the array.

"Adding" to a pointer increases the position at which it points:
- Adding 1 to an integer pointer points to the next `int`, add 4 bytes
- Adding 1 to a double pointer points to the next `double`, add 8 bytes

