---
tags: CMSC_132
created: 2025-11-7
description: 11/7, 11/10 notes (Lecture 28, 29)
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

### What makes a hash function good?

Hashing every key to 0 (using the function `hashFunction(key) = 0`) would satisfy the definition of a hash function (mapping a key to a value), but it isn't exactly a good one (because every key has the same value, so it's hard to access using a key and collisions will occur).

A good hash function:
- *Scatters* (distributes) values as uniformly as possible across the range of possible values, to reduce the likelihood of collisions and clustering
- Is not expensive (in terms of time) to compute

A hash function does not have to be perfect to be used.

The division method can be used as a compression function, but does not scatter values well in some cases.