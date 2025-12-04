---
tags: CMSC_132
created: 2025-11-7
description: 11/7, 11/10, 11/12, 11/14 notes (Lecture 28, 29, 30, 31) plus Sets & Maps handout
---

# Hashing

### Motivation

- We want to insert, lookup, and delete elements from an array as fast as possible, accessed by their keys
- Possible by using a really big array (we don't care how much memory is used) and using the key to find the element
- Problem is that there is a lot of empty space in the array, and it uses a lot of memory

### Hashing Concepts

A **hash function** is a function that maps a key to an integer.

The value produced by a hash function applied to a key is called a **hash code** or **hash value**.

The idea is to use a hash function to convert a key to a hash value that will be used as an index into an array (*hash table*), but it requires that the keys are unique.

### Compression Function

- Consider a hash table `h` of size `n`
	- Its indices (subscripts) range from 0 to `n - 1`
	- The hash function value must be restricted to the range 0...`n - 1`
	- A function that does this is called a **compression function**
	- The simplest compression function - the *division method* - just use modulus
- To know where in a hash table to store a key (i.e. which array position), use `Math.abs(compressionFn(hashFn(key))`
	- We need to take the absolute value because the compressed hash value could be negative

### Collisions

When multiple keys hash to the same has table location (array element) through the modulus/remainder, it's called a **collision**.

A *perfect* hash function produces a unique value for each key (but this usually isn't possible).

Collisions can be handled in one of several ways:
- *Bucket* or *chained* hashing (also called *separate chaining*)
- *Linear probing*
- *Double hashing*

##### Bucket or chained hashing

Each element of the hash table stores not just a single value, but a collection of values
- Each table entry is called a **bucket**
- Each bucket can be implemented using a list (the elements hashing to the same bucket are placed in the same list), or a binary search tree, or some other data structure
- If more than one element goes inside a bucket, have the data structure point to all of the other elements in that same hash table position

##### Linear probing

Each position of the hash table stores just one element, and if an element hashes to an occupied location when inserting, it's put in the next (following) empty location

Issues that have to be addressed with linear probing:
- Being able to tell whether an array element is occupied
- The index variable may be incremented past the array's size
- **Clustering**: when a sequence of keys become stored in consecutive array locations

Lookup/search algorithm:
- Compute `Math.abs(compressionFn(hashFn(key))`
- Start looking beginning at that position (the result of the above function) of the hash table
- If data is found with a matching key, the search succeeds

If we are searching for a key with linear probing, we know a key is not in the hash table if we find a `null` value/element when searching for it.

The number of *probes* refers to how many array elements are examined in the process of inserting/searching/deleting an element.

Deletion algorithm:
- Compute `Math.abs(compressionFn(hashFn(key))`
- Start looking beginning at that position of the hash table
- If key is found, mark its location as empty (this means storing a *tombstone* or *dummy value* in the location where the key being deleted is)

An insertion can store a key where nothing had ever been stored, or can reuse a location where an element was deleted (i.e. where a tombstone is), but *must* still search to the end of the cluster to ensure that the element isn't already in the table (because hash tables can't have duplicate keys).

If there are multiple tombstones encountered in doing an insertion, the element will be stored where the first one is seen (*after* searching to the end of the cluster).

##### Double hashing

Instead of searching sequentially (one by one) for the next empty position in the hash table when collisions occur, a second hash function is applied to the key, and the result of this hash function is added to the index/position continuously as long as occupied locations are seen.

Insertion/search pseudocode:
- `index = Math.abs(compressionFn(hashFn1(key)))`
	- `hashFn1()` is the primary hash function
- While `hashTable[index]` is occupied, `index = index + hashFn2(key)`
	- `hashFn2()` is the secondary hash function
- Store data in `hashTable[index]`

If we want to find what value(s) hash to position $X$ in a hash table using 2 probes with double hashing, we need to find $h_1$ (value of the first hash function) and $h_2$ (value of the second hash function) such that $h_1 + h_2 = X$. First, get the positions in the hash table before $X$ that are occupied. Then, for each of those positions, find the range of values that would equal that position in the first hash function (which would be $h_1$), and see if any of them equal $h_2$ in the second hash function. If any of them do, then that value hashes to position $X$ using 2 probes with double hashing.

### What makes a hash function good?

Hashing every key to 0 (using the function `hashFunction(key) = 0`) would satisfy the definition of a hash function (mapping a key to a value), but it isn't exactly a good one (because every key has the same value, so it's hard to access using a key and collisions will occur).

A good hash function:
- *Scatters* (distributes) values as uniformly as possible across the range of possible values, to reduce the likelihood of collisions and clustering
- Is not expensive (in terms of time) to compute

A hash function does not have to be perfect to be used.

The division method can be used as a compression function, but does not scatter values well in some cases.

### Writing hash functions in Java

The `Object` class' `hashCode()` returns the object's memory address as the numerical hash value for any object, so classes like `HashSet`, `HashMap`, etc. use it as their hash function.

However, a class can override the default `hashCode()` method with a user-defined version, but it must satisfy Java's "`hashCode()` contract" by working with `equals()`.

> [!info] Java's `hashCode()` Contract
> If `a.equals(b)` is true, we must guarantee that `a.hashCode() == b.hashCode()` .
> 
> However, `a.equals(b)` being false does not mean `a.hashCode() != b.hashCode()`, and `a.hashCode() == b.hashCode()` does not mean `a.equals(b)` is true.
> 
> `hashCode()` must return the same value for an object each time it's called while a program is run, if the values of fields used by `equals()` haven't changed.
> 
> A `hashCode()` method can only use the information/fields used by `equals()`, ensuring that two "equal" objects have the same hash value and reducing the likelihood of having the same hash value for unequal objects.
> 
> If a class implements the `Comparable` interface and there is a `compareTo()` method, the `hashCode()` method should be consistent with this (along with `equals()`).

Note: The default `equals()` and `hashCode()` methods do satisfy the hash code contract since two objects would be considered equal only if their memory addresses are equal, and the default hash code function uses the memory addresses of the objects and the two objects that are equal would have the same memory addresses, so their hash code values are equal as well.

If we override `equals()` in a Java class, it's a good idea to override `hashCode()` as well (otherwise we won't be able to correctly put objects of the class into a Java library set or use them as keys for a map).

### Important issues about hashing

Generally, the hash table should be big enough such that it has a load factor of no greater than 0.7-0.75 (after that, performance starts to degrade), so about $N/0.7$ or $N/0.75$ spaces (where $N$ is the maximum number of items that we know).

If a hash table becomes too full and we want to move the values to another larger hash table, then we need to rehash/reinsert each individual key into the new table.

All data access operations (insertions, lookups, and deletions) can be done very fast in hash tables ($O(1)$ time), but the tradeoff is that it requires more memory.

# Sets

**Sets** are data structures in which the elements have no relationship between them (i.e. no predecessors or successors) or ordering (i.e. no front or top or back), and is only a collection of elements.

Sets cannot contain duplicate elements.

> [!info] The `Set<E>` Interface
> Java has a `Set` interface implemented by several different classes, and it has several methods:
> 
> - `boolean add (E element)`: Inserts the element `element` into its current object set (Returns `true` if the element wasn't already present and `false` if it was)
> - `boolean contains(Object o)`: Tests whether `o` is in the current object set, returning true if it is and false if not
> - `boolean remove(Object element)`: Removes `element` from the current object set, returning true if it was present (and removed) and false otherwise
> - `boolean isEmpty()`: Tests if the current object set is empty
> - `int size()`: Returns the size of the set
> - `void clear()`: Removes all elements from the set
> - `boolean addAll(Collection<? extends E> c)`: Adds all of `c`'s elements to the set
> - `boolean containsAll(Collection<?> c)`: Returns true if all of `c`'s elements are in the set and false if any of them aren't
> - `Iterator<E> iterator()`: Returns an iterator for this set

Java has several classes for sets, including `HashSet`, `LinkedHashSet`, and `TreeSet`.

`HashSet` is the primary Java library set class and is implemented using a hash table (so the elements must implement the `hashCode()` method). If you iterate over the elements in a `HashSet` they will not be iterated over in any predictable order.

`LinkedHashSet` is a subclass of `HashSet` that supports ordering of elements (using a linked list), meaning the elements of a `LinkedHashSet` will be iterated over in the order they were added to it. However, it requires more memory than a `HashSet` and its operations may take slightly longer to perform (since it also involves maintaining the linked list along with the hash table).

`TreeSet` uses a binary search tree to store elements, so its elements will be iterated over in increasing order. Elements in a `TreeSet` must be comparable (unlike the other two classes). The operations of a `TreeSet` are slower than those of a `HashSet` or a `LinkedHashSet` since it must maintain the sorted order.

# Maps

A **map** is an unordered collection or set of keys, where each key has an associated value. The key is used to look up, modify, or delete the associated value.

> [!info] The `Map<K, V>` Interface
> Java has a `Map` interface implemented by several different classes, and it contains several methods for map operations:
> 
> - `V put(K key, V value)`: Inserts the value `value` into the map associated with the key `key` (or updates the value associated with `key` if key was already in the map). Returns `null` if `key` wasn't already a key in the map or returns the previous value if it was.
> - `V get(Object key)`: Returns the value associated with the key `key` in the map, or `null` if key is not a key in the map.
> - `V remove(Object key)`: Removes `key` and its associated value in the map, and returns the value removed (or `null` if `key` wasn't a key in the map)
> - `boolean isEmpty()`: Returns true if the map has no key/value pairs and false if it does
> - `int size()`: Returns the number of key/value pairs in the map
> - `boolean containsKey(Object key)`: Returns true if `key` is a key in the map, and false otherwise
> - `boolean containsValue(Object value)`: Returns true if `value` is a value in the map (meaning it is mapped to one or more keys), and false otherwise
> - `Set<K> keySet()`: Returns a `Set` containing all of the keys in the map
> - `Collection<V> values()`: Returns a `Collection` containing all of the values in the map (the `Collection` must be able to support duplicates since there could be duplicate values)

Note: If we modify a key set, then the map that the key set was generated from will also be modified. The same applies to the collection of values.

Java has several classes for sets, including `HashMap`, `LinkedHashMap`, and `TreeMap`. They do the same thing as the classes mentioned above for the `Set` interface except with maps instead.

Maps could also be implemented using two parallel unsorted arrays, or we could sort them by key, or using a single array of key/value pairs (objects).

Binary search trees are often used to implement maps, where each nonempty element contains a key, the associated value, and left and right child references. Because of this, it is necessary that we are able to compare the key (by having a generic type extend `Comparable` or using a `Comparator`).