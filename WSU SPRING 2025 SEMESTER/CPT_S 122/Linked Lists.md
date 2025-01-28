---
tags: CPT_S_122
created: 2025-1-21
description: Lesson 2.1
---

- **Linked list**: finite sequence of nodes, where each node may be only accessed sequentially (through links or pointers), starting from the first node
	- Also a linear collection of self-referential structures connected by pointers
	- The idea is that each node in a linked list points to the next node, which points to the next, and so on until we reach the end (a NULL pointer)

```
// this struct will be used for the examples

typedef struct node
{
	char data;
	// self-referential
	struct node *pNext;
}
```

### Initializing a List

- Initializes the list L to empty
```
void initList (Node **pList)
{
	// Recall: we must dereference a pointer to retain changes
	*pList = NULL;
}
```

- The `initList()` function is elementary and is not always implemented
- We may instead initialize the pointer to the start of the list with NULL within `main()`

```
int main(void)
{
	Node *pList = NULL;
}
```

### Checking for Empty List

- Returns TRUE if L is empty

```
int isEmpty (Node *pList)
{
	int status = 0; // False initially

	if (pList == NULL) // The list is empty
	{
		status = 1; // True
	}

	return status;
}
```

### Printing Data in List

Either of the two methods below can work (one is iterative and one is recursive):
```
void printListIterative (Node *pList)
{
	printf("X ->");
	while (pList != NULL) // could also say !isEmpty(pList) here
	{
		printf("%c -> ", pList->data);
		// Get to the next item
		pList = pList -> pNext;
	}
	printf("NULL\n");
}

void printListRecursive(Node* pList)
{
	// base case
	if (pList == NULL) { // if there is no node/list item
		printf("-->\n");
	}
	else { // recursive step
		printf("--> %s, %d", pList->data);
		printListRecursive(pList->pNext); // passes in the node the current node/list item is pointing to (this is the next node in the list)
	}
}
```

- We can determine the end of the list by searching for the NULL pointer
- If the list is initially empty, no problem, the while loop will not execute

### Inserting Data at Front of List

- Insert a node with information "e" into L as the first node in the List; in case L is empty, make a node containing "e" the only node in L and the current node
	- If the list is not empty, then this node will point to the node that was originally at the front of the list

##### Without error checking

```
Node *makeNode (char newData)
{
	Node *pMem = NULL;

	pMem = (Node *) malloc(sizeof(Node));
	// Initialize the dynamic memory
	pMem->data = newData;
	pMem->pNext = NULL;

	return pMem;
}

void insertFront (Node **pList, char newData)
{
	Node *pMem = NULL;

	pMem = makeNode(newData);

	// Insert the new node into front of list
	pMem->pNext = *pList; // new node points to node originally at the front
	*pList = pMem; // this node is the new node at the front
}
```

##### With error checking

- Checking for dynamic memory allocation errors

```
Node *makeNode (char newData)
{
	Node *pMem = NULL;

	pMem = (Node *) malloc(sizeof(Node));
	
	if (pMem != NULL)
	{
		// Initialize the dynamic memory
		pMem->data = newData;
		pMem->pNext = NULL;
	}
	// Otherwise no memory is available; could use else, but it's not necessary

	return pMem;
}

void insertFront (Node **pList, char newData)
{
	Node *pMem = NULL;

	pMem = makeNode(newData);
	
	if (pMem != NULL) // Memory was available
	{
		// Insert the new node into front of list
		pMem->pNext = *pList;
		*pList = pMem;
	}
	else // Can't allocate anymore dynamic memory
	{
		printf("WARNING: No memory is available for data insertion!\n);
	}
	
}
```