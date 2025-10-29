---
tags: CMSC_132
created: 2025-9-7
description: 9/3, 9/5, 9/8 notes (Lectures 1, 2, and 3)
---

### Keeping Data Private

- Use `private` keyword (for variables, methods, etc.)
- Use getter and setter methods to modify or access private fields

### Runtime Stack vs. Heap

The runtime stack and heap are the two areas of memory in a Java program.

Local variables and parameters (of a method/function) are stored in the runtime stack.

The heap contains all objects and arrays.

### Copying Objects

- **Reference copy**: Makes a copy of the reference of an object
	- Both the copy and the original point to the same location in memory
	- Changes to any field in the copy changes the corresponding field in the original as well (since they have the same address)
	- Safe if you have an immutable class
	- Fastest and uses least memory
- **Shallow copy**: Makes a copy of the object, but not object it refers to
	- In other words, makes direct copies of primitive variables (int, char, etc.) but not for reference fields (arrays, probably strings as well in Java)
	- Changes to any field that is a reference changes the corresponding field of the original as well, but NOT for primitive fields (since primitive fields are directly copied and aren't references)
- **Deep copy**: Makes a copy of the object AND all objects referred to by it (making it a completely independent object)
	- Changes to ANY field (regardless of whether it is primitive or a reference) does NOT change the original
	- Necessary when you want a completely independent duplicate of an object, particularly with reference fields, to prevent changes in the copy from affecting the original

> [!example]
> ```
> class Aardvark {
> 	private String name;
> 	private int weight;
> 	private double tongueLength;
> 	
> 	Aardvark() {
> 	...
> 	}
> }
> ```
> 
> Question: Write a copy constructor of `Aardvark` which does a deep copy.
> 
> Answer:
> ```
> Aardvark(Aardvark copyAardvark) {
> 	name = new String(copyAardvark.name);
> 	weight = copyAardvark.weight;
> 	tongueLength = copyAardvark.tongueLength;
> }
> ```

### `static`

Static fields means that it is a field that is shared among all objects of a class and isn't tied to a specific object.

Static methods means that it has no current object, so it *cannot refer to the object's non-static fields*. 

This means non-static fields *can only be used in non-static methods*, while static fields can be used in *both static and non-static methods*.