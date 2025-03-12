---
tags: CPT_S_122
created: 2025-3-10
description: Lesson 9.3
---

### Analysis of Algorithms

- Order of magnitude ("Big-O")
	- Any algorithm whose work can be expressed as c \* n where c is a constant and n is the input size is said to be "order of magnitude n", or O(n)
	- Likewise, any algorithm whose work varies as a constant times the square of the input size is said to be "order of magnitude n-squared", or O(n$^2$)
- Big-O analysis of Sequential Search
	- Best case: O(1)
	- Worst case: O(n)
	- Average case: O(n/2) = O(n)

### Selection Sort Algorithm Analysis

- Input: a list of numbers
- Output: a list of the same numbers in ascending order
- Method:
	- Set marker that divides "unsorted" and "sorted" sections of list to the end of the lsit
	- While the unsorted section of the list is not empty
		- Find largest value in "unsorted" section of list
		- Swap with last value in "unsorted" section of list
		- Move marker left one position
- Big-O analysis
	- Units of work: comparisons and exchanges
	- In all cases, we need *n + (n - 1) + ... + 1* comparisons = *\[n * (n - 1)] / 2* comparisons = *1/2n^2 - 1/2n* comparisons = O(n$^2$) comparisons
	- In best case, items are already in order, so 0 exchanges needed: O(n$^2$) comparisons + 0 exchanges = O(n$^2$)
	- In worst case, items are in reverse order, so *n* exchanges needed: O(n$^2$) + *n* exchanges = O(n$^2$)
- Space analysis
	- Major space requirement is list of numbers (n)
	- Other space requirements:
		- Extra memory location needed for marker between sorted and unsorted list
		- Extra memory location needed to store LargestSoFar used to find largest item in unsorted list
		- Extra memory location needed to exchange two values
		- Overall, space requirement is proportional to n

### Binary Search Algorithm Analysis

- Input: a list of n sorted values and a target value
- Output: True if target value exists in list and location of target value; False otherwise
- Method:
	- Set startIndex to 1 and endIndex to n
	- Set found to false
	- While found is false and startIndex is less than or equal to endIndex
		- Set mid to midpoint between startIndex and endIndex
		- If target equals the item at mid then set found to true
		- If target is less than the item at mid then set endIndex to mid - 1
		- If target is greater than the item at mid then set startIndex to mid + 1
- Big-O analysis
	- Unit of work: comparisons
	- Best case: target value is at first midpoint
		- O(1) comparisons
	- Worst case: target value is not found
		- List is cut in half until it is reduced to a list of size 0 (startIndex is greater than or equal to endIndex)
		- The list of size n can be cut in half $\log_2(n)$ times
		- O(log(n)) comparisons

### Orders of Magnitude

![[3.10.25 Orders of Magnitude Table.png]]