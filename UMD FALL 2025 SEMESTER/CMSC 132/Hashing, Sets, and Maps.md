---
tags: CMSC_132
created: 2025-11-7
description: 11/7 notes (Lecture 28)
---

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

##### Linear probing

Each position of the hash table stores just one element, and if an element hashes to an occupied location when inserting, it's put in the next (following) empty location

Issues that have to be addressed with linear probing:
- Being able to tell whether an array element is occupied
- The index variable may be incremented past the array's size
- **Clustering**: when a sequence of keys become stored in consecutive array locations