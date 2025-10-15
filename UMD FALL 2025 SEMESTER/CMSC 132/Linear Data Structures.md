---
tags: CMSC_132
created: 2025-10-1
description: 9/29 notes
---

A **list** is an abstraction of an expandable group of elements where each element has a position or index (there is a one-to-one relationship between elements).

Lists can be searched by value, index, preceding/succeeding element, properties of location, time added, etc.

Elements often added at the front or back of a list, after a particular element, at a particular position/index, etc. and often removed from the front or back, at a particular position/index, or one with a particular value.

### Linked List

Contains a head `Node` object, which contains data and a next `Node` object

```
class List {
	private Node head;
	...
}

class Node {
	private Object data;
	private Node next;
	...
}
```

If we want to have the `List` class access `Node` fields, make `Node` an inner class inside the `List` class so that they can access each other's private fields. It's probably best to make it a `private static` inner class as well.

### Linked List Insertion

If we want to insert `newNode` after node `n1` and before node `n2`, first have `newNode` point to the reference of `n2`, then have `n1` point to `newNode`.

### Linked List Deletion

If we want to delete a node, find the previous node and set it's next node to the current node's (the one we are deleting) next node.

### Linked List Variations

Standard linked list:
```
class List {
	private static class Node {
		private Object data;
		private Node next;
		...
	}
	
	private Node head = null;
}
```

Other variations include:
- **Circular linked list**: Tail node points to head node
- **Ordered list**: The nodes are ordered by their value
- **Doubly linked list**: Each node has a next and previous node reference
- **Maintaining a tail reference**
- **Dummy head node**: First node in the list doesn't have a value and is never used

### Ordered Lists

> [!info] Inserting into Ordered List between 2 Nodes
> If we want to insert `newNode`:
> 1. Iterate through list until we find the first node whose value is greater than `newNode` (call this `n2`)
> 2. The node before `n2` will be `n1`, which is the previous node
> 3. Have `n1`'s next node point to `newNode` and `newNode`'s next node point to `n2`

> [!info] Inserting into Ordered List at the Front
> If we want to insert `newNode`:
> 1. Have `newNode`'s next node refer to the current head node
> 2. Set `newNode` as the new head node

> [!info] Inserting into Ordered List at the Back
> If we want to insert `newNode`:
> 1. Find the last node in the list and have it's next node point to `newNode`

It is slower to add elements but faster to search for them in ordered lists.
It is faster to add elements but slower to search for them in unordered lists.

### Doubly Linked List

Every element has a reference to its successor and a predecessor.

```
class Node {
	private Object data;
	private Node next;
	private Node prev;
	...
}
```

Advantages:
- Easy to find both succeeding and preceding elements
- List manipulation may be easier than with singly-linked list

Disadvantages:
- Extra work to maintain references when inserting or deleting
- Uses more memory per node than a singly-linked list

### Doubly Linked List Insertion

To insert `newNode` between `n1` and `n2`, have `n1`'s next node refer to `newNode` and `newNode`'s previous node refer to `n1`.

In addition, have `newNode`'s next node refer to `n2` and `n2`'s previous node refer to `newNode`.

### Doubly Linked List Deletion

To delete `newNode` (assuming it's between nodes `n1` and `n2`), have `n1`'s next node refer to `n2` and `n2`'s previous node refer to `n1`, then delete `newNode`

### Dummy Head Node

A list's head reference can be set to a dummy head or first node when the list is created.

The value of the first node (which is usually empty) isn't ever looked at or used.

Avoids special cases for an empty list, or the beginning of the list, in some methods.

The head pointer is never `null`, even for an empty list, and the head pointer is never changed after the dummy head node is created.

```
class List {
	private static class Node {
		...
	}
	
	final Node head = new Node(null);
}
```

### Array Implementation of a List

Advantages:
- Uses memory space efficiently
- The element at any position can be accessed efficiently

Disadvantages:
- More work to insert or remove elements in the middle of a list (need to move elements around)
- More work to grow or shrink the array
- Tricky to insert and remove elements at both ends if needed

`ArrayList` allows for easy access to elements while also having the ability to expand its size.

### Linked Implementation of a List

Advantages:
- Elements can be easily inserted and removed anywhere in a list

Drawbacks:
- Indexing is not possible to do efficiently, requires traversing from the head
	- **Indexing** is finding an element immediately in a list with a number
- It requires more memory space (1-2 additional references per element stored)

Java has a `LinkedList` library class (both it and the `ArrayList` classes have a common superclass, `AbstractList`)

### Linked List Data Type

It is possible to have the data field in `Node` classes be of type `Object`, but we can make it of the desired type, like `int`, or even make `Node` a generic class and have the data field be a generic type.

### Implementing `equals()`

The `equals()` method compares whether two objects have the same state, or values of all of their fields.

If an `equals()` method is not explicitly written, then the `equals()` method in the `Object` class is run, which checks if the memory addresses of the two objects are equal (not the values).

Five things that an `equals()` method must do or have:
1. Parameter has to be of type `Object`
2. Must handle the parameter being `null` by returning false (so that the program won't have an error if `null` is passed in)
3. Must ensure its parameter is an object of the class the method is in (using `instanceof` or `getClass()`) so that objects of two completely different instances/classes aren't being compared
4. Must cast its parameter to the class the method is in so that the program can access the object's fields
5. If the parameter is valid, must compare all fields of the casted parameter to the fields of the current object, returning true if they have all the same values, and false otherwise

We don't want to compare objects using reference comparison, and can't compare objects by comparing string representations either.