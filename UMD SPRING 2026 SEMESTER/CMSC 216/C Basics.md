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

### Allocating Memory

Most C data has a fixed size, being single variables or arrays with sizes specified at compile time.

`malloc(nbytes)` is used to manually allocate memory, while `free()` is used to release memory.

`sizeof()` is commonly used with `malloc()` . It's more useful for getting the size of data types and structs and less useful for finding array sizes.

### The 4 Logical Regions of Program Memory

1. **Stack**: Automatic, push/pop with function calls
2. **Heap**: `malloc()` and `free()`
3. **Global**: Variables outside of functions, `static` variables
4. **Text**: Program instructions in binary

The stack grows towards the heap, and a collision results in *stack overflow*.

The global and text regions are usually fixed in size.

### `struct`

`struct`s are heterogeneous groupings of data, where each **field** can be of a different type

Each instance of a `struct` has all of its fields.

Access elements with "dot" notation.

Example:
```
typedef struct {
	int an_int;
	double a_doub;
	char the_car;
	int my_arr[6];
}

thing_t a_thing;
a_thing.an_int;
a_thing.a_doub;
a_thing.the_char;
a_thing.my_arr[2];
```

`struct`s can have pointers to their same kind. In that case, to access fields, we need to use the `->` operator (Note: for an *actual* struct, not a *pointer to a struct*, then we would use the "dot" operator).

Use `sizeof()` to dynamically allocate memory for structs.

### Reading into Variables

`scanf()` is used to take user input.

Use `%s`, `%d`, and `%lf`/`%f` for strings, integers, and doubles respectively.

Need `&` operator for integers/characters/doubles, but not for strings.

### File Input and Output

`FILE *fopen(char *fname, char *mode)`: opens a file (returns NULL if unsuccessful)

`int fclose(FILE *fh)`: closes a file and frees memory

`int fscanf(FILE *fh, char *format, addr, addr2, ...`: reads data from a file (returns EOF if end of file is reached)

`int fprintf(FILE *fh, char *format, arg1, arg2, ...`: prints data to a file

`void rewind(FILE *fh)`: returns the given open file handle to the beginning of the file