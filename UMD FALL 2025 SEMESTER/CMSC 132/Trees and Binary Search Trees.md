---
tags: CMSC_132
created: 2025-10-22
description: 10/22, 10/24, 10/27, 10/29, 10/31 notes (Lectures 21, 22, 23, 24, and 25)
---

**Trees** are self-referential data structures that have a one-to-many relationship between elements.

A tree element:
- Usually contains some data
- Can have *any number* of other elements after it (its *children*)
- Is the child of at most one other element (its *parent*)

### Tree concepts

The **root** is the element in the tree with no parent (there is only 1).

A **leaf** is an element in the tree with no children (there can be multiple).

**Interior elements** are elements with children (anything that isn't a leaf).

**Siblings** are elements with the same parent.

**Descendants** are elements that are children of another node's children (and would be a descendant of that node's parent, and the parent's parents, etc.).

**Subtree** consists of an element and all of its descendants.

**Depth** is a measure of an element's distance from the root (the root would have a depth of 0, and the depth of any other element is one more than its parent's depth).

The **height** of a tree is the maximum depth of any element in the tree.

### Binary Trees

A **binary** tree is a tree with at most two children per element, which are referred to as the element's left and right children and indicate its left and right subtrees.

Implementation:
```
public class Tree {
	private static class Node {
		private Object data;
		// left/right will be null if no child
		private Node left;
		private Node right;
	}
	
	private Node root = null; // empty tree
}
```

### Tree Traversal

- A *depth-first* traversal visits elements as far ahead as possible before backing up
	- A **preorder** traversal visits/processes an element first, then its left child, then its right child
		- Note: The root node would be the first node in a preorder traversal; useful for if we want to construct a binary tree from a preorder traversal
	- An **inorder** traversal visits an element's left child, then the element itself, then its right child
	- A **postorder** traversal visits an element's left child, then its right child, then the element itself
		- Note: The root node would be the last node in a postorder traversal; useful for if we want to construct a binary tree from a postorder traversal
- A *breadth-first* traversal visits elements according to how far away they are from the root
	- Algorithm:
		- Create a queue
		- Enqueue the root element in the queue
		- While the queue isn't empty, dequeue (remove) the front element from the queue and process the element just removed
			- If the element has a left child, enqueue the left child in the queue
			- If the element has a right child, enqueue the right child in the queue

### Binary Search Trees

A **binary search tree** is a binary tree where every element is larger than all the values in its left subtree, and smaller than all the values in its right subtree.

### Searching for an element in a BST

If you are searching for a value `v` in a binary search tree, for the following cases:
- `v` is equal to the value of the node you're looking at: Stop searching, you have found the node
- `v` is less than the value in the node you're looking at: Go to this node's left subtree
- `v` is greater than the value in the node you're looking at: Go to this node's right subtree

### Constructing Binary Search Trees

At all times, the binary search tree property (that smaller values are in each element's left subtree and larger values are in its right subtree) must be maintained because the search properties rely on this.

### Binary Search Tree Insertion

Inserting a value `X`:
1. Perform a search for `X`
2. If `X` is not in the tree the search will end at an element `Y`
3. If `X < Y`, add a new leaf element containing `X` as the new left child of `Y`
4. If `X > Y`, add a new leaf element containing `X` as the new right child of `Y`

### Binary Search Tree Deletion

1. Perform a search for the value `X` to be deleted
2. If `X` is a leaf, just remove `X`
3. Else (must delete an interior element)
	1. Replace `X` with...
		1. the largest value `Y` in its left subtree OR
		2. with the smallest value `Z` in its right subtree
	2. Then delete the replacement value (`Y` or `Z`) from the subtree it came from (recursively)

### Balanced and Degenerate Binary Trees

A **balanced** binary tree has (mostly) two children per element.
- Note: The height of a balanced tree is $O(\log (n))$

A **degenerate** binary tree has (mostly) one child per element (more like a list).
- Note: The height of a degenerate tree is $O(n)$

### Efficiency of Binary Search Tree Operations

- Search or lookup (average case)
	- Balanced tree: $O(\log(n))$
	- Degenerate tree: $O(n)$
- Lookup and insertion (average case)
	- Balanced tree: $O(\log(n))$
	- Degenerate tree: $O(n)$
- Lookup and deletion (average case)
	- Balanced tree: $O(\log(n))$
	- Degenerate tree: $O(n)$