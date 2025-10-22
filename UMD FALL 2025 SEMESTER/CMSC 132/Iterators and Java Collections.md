---
tags: CMSC_132
created: 2025-10-21
description: 10/20 notes
---

### Iterating

Suppose we have a class storing a number of data elements. We would like to be able to process (iterate over) the elements, maybe from outside the class, without knowing exactly how they're being stored
- Why? (ANSWER LATER!!)
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

`remove()` is optional; can be called once after each call to `next()` to remove the element that `next()` just returned

### Creating iterators without problems

Let's say `MyIterator` is a class that implements `Iterator` and `MyList` is a list class.

- Define `MyIterator` as an inner class in `MyList`
- An instance of `MyIterator` will be tied to a `MyList` object
- `MyIterator` methods can then access private `MyList` fields and methods