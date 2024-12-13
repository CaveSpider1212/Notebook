---
tags: CPT_S_121
created: 2024-10-7
description: Lesson 8.1 - Arrays
---

### Arrays

- **Array**: sequence of items that are *contiguously allocated in memory*
	- Items in the array are of the same data type and size
	- Each item is referenced using a different index of the array, but they are all accessed with the same array name
	- They are data structures, which allow data to be manipulated easily
- Arrays can be single-dimensional (linear) or have multiple dimensions (two-dimensional is considered to have rows and columns)

```
int a[6]; // creates an array "a" with 6 spots

int b[] = {2, 5, 7, 9}; // creates an array "b" with integer values 2, 5, 7, 9 contained in it...no size needed
```

- Indexing in arrays start from 0 since it represents the "distance" from the memory space the array is located in
	- This is why when you pass in an array into a function, only the first element (at index 0) is copied and passed into the function
- We can do operations with entries of the array as if they were actual variables

### Array Searching

- **Sequential search**: search through the array in order and stop when the target is found
- **Binary search**: takes indices 1 and *n* (length of the array), as the starting left and right indices, respectively; also sets *m* to the midpoint between 1 and *n*, and moves *m* and *n* around depending on whether the target value is less than, equal to, or greater than the midpoint
	- If target = item at *m*, then the target has been found
	- If target < item at *m*, then the right index becomes *m* - 1
	- If target > item at *m*, then the left index becomes *m* + 1
	- **Note**: array must be already sorted to use binary search properly

### Array Sorting

- **Selection sort**: divides the list into sorted and unsorted parts starting from the beginning list, then takes the smallest value in the unsorted list and swaps it with the first value in the unsorted list, then moves the divider 1 position to the right and repeats

### Multidimensional Arrays

- **Multidimensional array**: contain multiple rows of values (single-dimensional arrays only had one row of values)

```
int arr[3][4]; // declares an integer array with 3 rows and 4 columns
```

### Accessing Values in Array

**Array notation**: `a[i]` where `a` is the array and `i` is the index
**Pointer notation**: `*(a + i)` where `a` is the array and `i` is the index