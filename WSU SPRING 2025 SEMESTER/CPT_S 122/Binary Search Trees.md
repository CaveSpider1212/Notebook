---
tags: CPT_S_122
created: 2025-3-10
---

### What a Binary Tree is

- A **binary tree** consists of a set *T* of nodes so that either:
	- *T* is empty (no nodes), or
	- *T* consists of a node *r*, the root, and two subtrees of *r*, each of which is a binary tree:
		- The *left subtree* and the *right subtree*

### Binary Tree Terminology

- **Child** and **Parent**: every node except the root has one parent; a node can have zero or more children
- **Leaves**: nodes with no children
- **Sibling**: nodes with same parent
- **Path**: a sequence of edges
- **Length of a path**: number of edges on the path
- **Depth** of a node: length of the unique path from the root to that node
- **Height** of a node: length of the longest path from that node to a leaf (all leaves are at height 0)
	- Height of a tree = height of the root = depth of the deepest leaf
- **Ancestor** and **descendant**: if there is a path from `n1` to `n2`, then `n1` is an ancestor of `n2` and `n2` is a descendant of `n1`

### Binary Trees ADT

- Data: a set of nodes
- Operations:
	- **Create** (empty)
	- **Create**, given a root and two subtrees
	- **Destroy**
	- **isEmpty**
	- **getRootData** and **setRootData**: access to data in a root node
	- **attachLeft** and **attachRight**: attach a child to the root
	- **attachLeftSubtree** and **attachRightSubtree**: attach a subtree to the root
	- **detachLeftSubtree** and **detachRightSubtree**: detach a subtree from the root
	- **leftSubtree** and **rightSubtree**: returns a subtree
	- **preorderTraverse**, **inorderTraverse**, and **postorderTraverse**: visit all nodes in the appropriate order

### Binary Search Tree

> [!info] BST Property
> All elements stored in the left subtree of a node whose value is ***K*** have values less than ***K***. All elements stored in the right subtree of a node whose value is ***K*** have values greater than or equal to ***K***.
> 
> That is, a node's left child must have a key less than its parent, and a node's right child must have a key greater than its parent.

![[3.10.25 BST.png]]

- Operations on BST ADT
	- Create a BST (create a node)
	- Insert an element (Node)
	- Remove an element (Node)
	- Find an element (Node)
	- Clear (remove all elements)
	- Display all elements in a sorted order
	- Traversals
	- Print the Tree in a "tree view" using a queue

##### Inorder Traversal

- **Inorder traversal**: visit the left subtree, then the node, then the right subtree
- Algorithm
	1. If there is a left child, visit it
	2. Visit the node itself
	3. If there is a right child, visit it

##### Postorder Traversal

- **Postorder traversal**: visit each node after visiting its children
- Algorithm
	1. If there is a left child, visit it
	2. If there is a right child, visit it
	3. Visit the node itself

##### Preorder Traversal

- **Preorder traversal**: visit each node then visit its children
- Algorithm
	1. Visit the node itself
	2. If there is a left child, visit it
	3. If there is a right child, visit it

##### Insert

1. If the value we want to insert is less than the key of the current node, we have to go to the left subtree
2. Otherwise, we have to go to the right subtree
3. If the current node is empty (not existing), create a node with the value we are inserting and place it here

![[3.10.25 Insert BST.png]]

##### Delete

- Node to be deleted has no children
	- We just delete the node
- Node to be deleted has only one child
	- Replace the node with its child and the *parent* of the deleted node be a parent of the *child* of the deleted node
- Node to be deleted has two children
	- Find minimum value of right subtree
	- Replace the value of the node to be deleted by the minimum value
	- Delete minimum node of right subtree

![[3.10.25 Delete from BST 2 children.png]]