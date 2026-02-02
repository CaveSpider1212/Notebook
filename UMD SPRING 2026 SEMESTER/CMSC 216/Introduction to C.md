---
tags: CMSC_216
created: 2026-1-28
description: 1/27, 1/29 notes
---

Most computers have 4 basic, physical components:
- **CPU**: can execute "instructions"
- **Control**: CPU knows which instruction to execute
- **Memory**: data is stored and can change
- Input/Output devices like a **screen**

CPU understands some *set of instructions*; a sequence of instructions is a *program* that changes memory and the screen.

Memory cells have a fixed *address* but changeable *contents*.

**Random Access Memory (RAM)**: the contents in any memory cell can be retrieved fast using its address.

### Variables

**Variables** are named memory cells.

The compiler/interpreter automatically translates the variable name to the corresponding memory cell/address.

### Correspondence of C Programs to Memory

C programs require memory cell names to be declared with the *type of data* they will hold.

The equal sign (=) means "store the result on the right in the cell named on the left."

```
int x; // indicate a new memory cell with name "x" is needed
x = 42; // put 42 in cell x
int y = 31; // indicate a new memory cell with name "y" is needed, and put 31 in it
```

### Motivation for C

Languages like Java and Python provide many safety and convenience features, and also insulate the programmer from hardware for ease-of-use (being high-level languages).

C presents many CPU capabilities directly, and as a result has very few safety features and there is little between the programmer and the hardware.

### Von Neumann Machine Architecture

- Processing
	- Wires/gates that accomplish fundamental operations (including +, -, \*, AND, OR, move, copy, shift, etc.)
	- Operations act on contents of memory cells to change them
- Control
	- Memory address of next instruction to execute
	- After executing, move ahead one unless instruction was to jump elsewhere
- Memory
	- Giant array of bits/bytes, so *everything* is represented as 1's and 0's, including instructions
	- Memory cell contents accessible by address number
- Input/Output
	- Allows humans to interpret what is happening
	- Often special memory locations for screen and keyboard

### Direct Use of Memory Cell Address

C allows for direct use of memory cell addresses

- `&x` (**Address of**): Memory address of variable `x`
- `int *a` (**Pointer variable**): The variable `a` stores a memory address
- `*a` (**Dereference**): Get/set the value pointed to by `a`

Pointers and memory addresses allow us to change the values of variables declared in one function in another function (by having pointer variables in the parameters of the second function, and passing the addresses of the variables when calling that function in the first function).

```
void swap_ptr(int *a, int *b);

int main(int argc, char *argv[]) {
	int x = 42;
	int y = 31;
	swap_ptr(&x, &y);
	printf("x: %d y: %d\n", x, y); // prints "x: 31 y: 42"
	return 0;
}

// Swaps the values of a and b
void swap_ptr(int *a, int *b) {
	int tmp = *a;
	*a = *b;
	*b = tmp;
	return;
}
```

In the above code, `&x` and `&y` pass in the memory addresses of the variables `x` and `y` into the function. The values associated with `a` and `b` in the function become the memory addresses of the `x` and `y` memory cells, respectively.

`*a` essentially operates on the cell pointed to by `a` (so `x`). The pointer dereference on the right side *fetches* a value from a pointer location (so in this case, fetches the value from the cell pointed to by `b`, which is `y`). The pointer dereference on the left side *stores* a value at a pointer location (so in this case, stores the value into the cell pointed to by `a`, which is `x`).

(see [[Dynamic Data Structures]])

Note: `a` and `b` are pointers, so they cannot be changed. `x` and `y`, on the other hand, are only variables, so they can be changed.

Due to the function call stack (the swap function having its own local variables in memory and the main method having its own variables), the contents of the variables/memory cells cannot be changed in the other function without pointers.

Pointers allow any line of C programs to modify any of its data. This allows for fine control of memory, leading to efficiency and using the machine's true capability, but also opens up many errors not possible in Java/Python which restrict use of memory.