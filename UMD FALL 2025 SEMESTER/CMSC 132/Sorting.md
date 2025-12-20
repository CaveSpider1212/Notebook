---
tags: CMSC_132
created: 2025-12-9
description: 12/5, 12/8, 12/10 notes (Lecture 38, 39, 40)
---

### Sorting

**Sorting** refers to rearranging a list of elements in order based on the key for each element.

Sorting algorithm properties:
- A *stable* sort preserves the original order of duplicate keys
- An *in-place* sort only uses a constant amount of additional memory (no new data structures created)
- An *external* sort sorts data that's not all in memory at the same time

### Types of sorting algorithms

A *comparison* sort only uses pairwise key comparisons.

Comparison sorts have a lower bound efficiency of $n \log n$, meaning it cannot be done more efficiently than that.

A *linear* sort is more efficient than a comparison sort, but requires knowing additional information in advance about the keys to be sorted.

Linear sorts have a lower bound efficiency of $n$.

### Bubble sort

- Approach:
	- Repeatedly sweep through shrinking portions of the list of elements remaining to be sorted
	- Swap an element $x$ with the element following it if $x$ is larger

Bubble sort has $O(n^2)$ time complexity for the average and worst cases (if the array is in reverse order), and $O(n)$ for the best case (if the list is already sorted).

We compare one key to another each time, so it's a comparison sort.

It is in-place since no additional memory is involved.

This algorithm is inefficient.

This sort is stable since if two elements are equal, the elements are not moved (they're only moved if the left element is greater than the right).

### Selection sort

- Approach:
	- Repeatedly sweep through shrinking portions of the list
	- Select the smallest element found in each sweep
	- Swap the smallest element with the first one in the remaining unsorted part of the list

Selection sort has $O(n^2)$ time complexity for all cases (average, worst (list is in reverse order), and best (list is in order)).

We compare one key to another each time, so it's a comparison sort.

It is in-place since no additional memory is involved.

This algorithm is always inefficient.

This sort can be stable since the minimum element does not change if an element equal to the minimum is found (only changes when a value *less* than the minimum is found).

### Insertion sort

- Approach:
	- The sorted part of the array is on the left, and the unsorted part is on the right
	- At every step the first (leftmost) element of the unsorted part of the array ($x$) is added to the sorted part in between the elements less than $x$ and the elements greater than $x$.

Insertion sort has $O(n^2)$ efficiency in the average and worst cases (when the array is sorted in reverse order). In the best case (when the array is in order), it has $O(n)$ comparisons and $O(1)$ swaps.

It involves comparing two keys at a time, so it's a comparison sort.

It is in-place since no extra memory is involved.

This sort can be stable since the current element will keep being moved to the left while it is less than the previous element (does not stop if an element is equal to it, so the relative order is preserved).

### Tree sort

- Approach:
	- Insert elements in a binary search tree
	- Copy the elements back to the array using an inorder traversal

Tree sort has $O(n \log n)$ efficiency in the average and best cases (if the tree is balanced), and $O(n^2)$ efficiency in the worst case (if the tree is degenerate).

Since it involves comparing two keys at once while constructing the tree, it is a comparison sort.

This is NOT in-place since extra memory (for the binary search tree) is involved in this algorithm.

This is also an unstable sort since binary search trees can't have duplicate elements.

### Heap sort

Heap sort uses a max heap to sort values. The heap makes it easy to remove the largest element, which is done repeatedly.

- Algorithm:
	- Create a max heap
	- Insert the values to be sorted in the heap
	- Remove the values from the heap using `getLargest()` and copy them to the array, from back to front (they'll be in ascending order)

Heap sort has $O(n \log n)$ efficiency in all cases (since heaps are always balanced).

This algorithm involves comparing values when constructing the max heap, so it is a comparison sort.

This algorithm is an unstable sort since elements could be rearranged when creating the heap.

This can be either in-place or not in-place depending on if we use the array itself for heap sort or use a separate binary tree.

### Quick sort

- Approach:
	- Select one of the elements, called the pivot value
	- Partition the elements (into two lists) using the pivot value
		- All elements less than the pivot value goes in one list, while all elements greater than the pivot value goes in the other list
	- Recursively sort the resulting lists
		- Call the method again on the two lists (the values less than and greater than the pivot)
	- Concatenate the resulting lists (if not sorting in place)

Quick sort has $O(n \log n)$ efficiency in the average and best cases (when the pivot value is in the middle of the list each time), and $O(n^2)$ efficiency in the worst case (when the pivot value is at either end of the list or if the list is sorted).

This algorithm can be done in-place or not in-place.

It involves comparing keys against the pivot value, so it's a comparison sort.

This is not a stable sort since the partitioning does not take into account their original positions.

### Merge sort

- Approach:
	- Divide the list of elements to be sorted into two sublists
	- Recursively sort both sublists
	- Merge both sorted sublists into one sorted list:
		- Examine the front elements of both sublists
		- Move the smaller of these to the end of the new list
		- Continue until both sorted sublists are empty

Merge sort has $O(n \log n)$ efficiency in all cases. The worst case occurs when the maximum comparisons are needed when merging, and the best case occurs when the list is already sorted (but it still divides and merges).

This algorithm requires extra memory for the merge operation, so it is NOT in-place.

It involves comparing two keys at once when merging the elements, so it is a comparison sort.

It can be stable because if two elements are equal, then the first element will always go in the left sub-array and be first in the merged array.

### Counting sort

- Sorts keys with values over the range $0 ... k$
- Approach:
	- Count the number of occurrences of each key
	- Calculate the number of keys that are less than or equal to each key
	- Place keys in their sorted location using the number of keys counted
		- If there are $x$ keys less than or equal to key $y$, put $y$ in the $x$th position
		- Decrement $x$ in case there are more instances of the key $y$

Counting sort has $O(n + k)$ efficiency, where $n$ is the number of elements being sorted and $k$ is the highest key. The number of operations depends on whether $n$ or $k$ is bigger.

This is not a comparison sort as two values are never compared at once. This is a linear sort since we must know information about the keys beforehand.

This is not in-place since there are other arrays that are created in this algorithm.

It can be stable.

### Radix sort

- Decompose each key $K$ into components $K_1, K_2, ..., K_d$
	- Component $d$ is the least significant
	- Each component has values over range $0 ... c$
- Example key components would be characters for keys that are strings, or digits for keys that are numbers
- Approach: Sort the keys by component, from the least significant to the most significant

Radix sort has $O(d \times (n + c)) \approx O(n)$ efficiency in the average and worst cases.

This is not a comparison sort since it does not directly compare pairs of items. Instead, it distributes elements into "buckets" based on the value of their current digit without comparing any two elements in the original list, so it's a linear sort.

This is not in-place since it requires additional memory space (buckets or arrays) to store the elements during each pass.

It can be stable since the elements' positions relative to each other are taken into account while sorting.