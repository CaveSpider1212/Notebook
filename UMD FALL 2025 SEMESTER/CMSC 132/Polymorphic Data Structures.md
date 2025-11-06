---
tags: CMSC_132
created: 2025-10-30
description: Notes from Lectures 18, 19, and 24
---

### Polymorphic List

Alternate implementation that can be used for lists (and some other data structures).

A list could be an interface, or a superclass. Implement two subclasses of it: `EmptyList` and `NonEmptyList`

**Polymorphic lists** contains zero or more `NonEmptyList` objects and always ends with an `EmptyList` object.

`EmptyList` is used to represent an empty list, and the end of a list, rather than `null`.

Allows you to invoke methods on elements without checking for `null`.

Implementation:
```
public interface List {
	NonEmptyList insert(Object data);
	...
}

public class EmptyList implements List {
	NonEmptyList insert(Object data) {
		...
	}
	...
}

public class NonEmptyList implements List {
	Object data;
	private List next; // Could refer to either an EmptyList or a NonEmptyList
	
	NonEmptyList insert(Object data) {
		...
	}
	...
}
```

The `EmptyList` and `NonEmptyList` implementations of a method can be different depending on what we want it to do when the list is empty or not empty.

### Polymorphic Binary Search Tree

```
public interface Tree {
	Tree isnert(Object data);
	...
}

public class EmptyTree implements Tree {
	Tree insert(Object data) {
		...
	}
	
	...
}

public class NonEmptyTree implements Tree {
	Object data;
	Tree left, right; // either Empty or NonEmpty trees
	
	Tree insert(Object data) {
		...
	}
	
	...
}
```

##### The singleton design pattern

`EmptyTree` could be a **singleton class**, where only one instance of a class or value is created that's accessible globally.

If any `NonEmptyTree` object does not have any left or right children, then it points to a singular `EmptyTree` object (all `NonEmptyTree` objects without left/right child point to this same one).

The advantage is that it saves memory (we don't need to have `EmptyList` objects each time a `NonEmptyTree` doesn't have a left/right child).

Making the constructor private ensures that only one object of a class can ever be created, as well as making the object static

```
public class Single {
	// Declares the unique instance of the class
	private static Single uniqueObj = new Single();
	
	// Constructor is private, so it can only be accessed from this class
	private Single() {
		...
	}
	
	// Returns a reference to the unique instance of the class
	public static Single getInstance() {
		return uniqueObj;
	}
}
```