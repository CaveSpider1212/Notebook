---
tags: CMSC_132
created: 2025-10-21
description: 10/20, 10/22 notes (Lectures 20 and 21)
---

### Iterating

Suppose we have a class storing a number of data elements. We would like to be able to process (iterate over) the elements, maybe from outside the class, without knowing exactly how they're being stored
- This allows us to keep the internal representation of the class private
- Mechanism in Java: the `Iterable` interface

```
public interface Iterable<T> {
	Iterator<T> iterator();
}
```

`iterator()` returns an `Iterator` over a group of elements of type `T`

### The `Iterator` interface

```
public interface Iterator<E> {
	boolean hasNext();
	E next();
	void remove();
}
```

`hasNext()` should return true if any elements haven't been returned by `next()` yet

`next()` should return some element

`remove()` is optional; can be called once (but *only* once) after each call to `next()` to remove the element that `next()` just returned

### Creating iterators without problems

Let's say `MyIterator` is a class that implements `Iterator` and `MyList` is a list class.

- Define `MyIterator` as an inner class in `MyList`
- An instance of `MyIterator` will be tied to a `MyList` object
- `MyIterator` methods can then access private `MyList` fields and methods

### The Iterator Design Pattern

See [[Design Patterns#^3e6c80]]

### The Java Collections Framework

Part of the Java library consisting of:
- Interfaces
- Implementations of data structures
- Algorithms (reusable functionality for the data structures)

### The `Collection` interface

- The root interface of Java's collection hierarchy
- Core operations:
	- Adding an element to a collection
	- Finding an element in a collection
	- Removing an element
	- Return a collection's size (number of elements)
	- Process all the elements in a collection
- Note that the methods that search for elements in a `Collection` use the `equals()` method to compare elements
- Additional operations supported by some collections:
	- Finding the first element
	- Find the kth element
	- Find the largest element
	- Sort the elements

![[11.2.25 Collections Hierarchy.png]]

### Important `Collections` methods

`boolean add(E e)`
`void clear()`
`boolean contains(Object o)`
`boolean isEmpty()`
`Iterator<E> iterator()`
`boolean remove(Object o)`
`int size()`

### The `Collections` class

- Just contains static methods that operate on `Collection`s
- A few of its methods include `sort()`, `shuffle()`, `copy()`, and `fill()`
- Note: The `Arrays` class has similar methods that operate upon arrays

### The `foreach` loop with iterators

- Works for arrays and any class that implements the `Iterable` interface, including all `Collection`s
- It handles the iterator automatically by testing `hasNext()`, then invoking `next()`

Note: By default it's incorrect to modify something while an iterator or a `foreach` loop is iterating over it, other than by calling `remove()` when using an explicit iterator (`remove()` can't be called when using a foreach loop)