---
tags: CPT_S_122
created: 2025-1-27
description: Lesson 3.2 and 4.1
---

### What is a Stack?

- **Stack**: a finite sequence of nodes, where only the top node may be accessed
- Insertions (pushes) and deletions (pops) may only be made at the top
	- Last in, first out (LIFO) data structure
- A stack is a restricted or constrained list

### The Function Call Stack

- LIFO
- Also called *program-execution* stack, *run-time* stack, *program* stack, or simply "the *stack*"
- Supports the function call/return *mechanism*
	- Necessary to track sequence of called functions
- Supports the *creation, maintenance*, and *destruction* of each called function's *local* variables
- Call stack memory placed in RAM, monitored closely by CPU
- When a function declares a variable, it is "pushed" onto the stack
	- Dynamic memory is not
- Parameters also passed using the call stack

### Heap

- **Heap**: region of memory not managed for you (unlike with the stack)
	- We need to explicitly deallocate (free) the memory

### Struct StackNode

```
typedef struct stackNode
{
	char data;
	// self-referential
	struct stackNode *pNext;
} StackNode;
```

### Initializing a Stack

- **InitStack(S)**: procedure to initialize the stack S to empty

```
void initStack(StackNode **pStack)
{
	// must dereference a pointer to retain changes
	*pStack = NULL;
}
```

- Can say `StackNode *pStack = NULL;` in `main()` instead (`*pStack` points to the top of the stack)

### Checking for Empty Stack

- **StackIsEmpty(L) -> b**: Boolean function to return TRUE if S is empty

```
int isEmpty (StackNode *pStack)
{
	int status = 0; // false initially

	if (pStack == NULL) {
		status = 1; // now true
	}

	return status;
}
```


### Printing Data in Stack

```
void printStackIterative (StackNode *pStack)
{
	printf("X -> ");

	while (!isEmpty(pStack)) {
		printf("%c -> ", pStack->data);
		// Get to the next item
		pStack = pStack->pNext;
	}

	printf("NULL\n");
}
```

### Inserting Data into a Stack

- **Push (S, e)**: insert information e into S; if S is empty, make a node containing e the only node in S and the current node
	- Can make separate function to create the node instead

##### Without error checking

```
void push (StackNode **pStack, char newData)
{
	StackNode *pMem = NULL;

	pMem = (StackNode *) malloc (sizeof(StackNode));

	// Initialize the dynamic memory
	pMem->data = newData;
	pMem->pNext = NULL;

	// Insert new node onto top of stack
	pMem->pNext = *pStack;
	*pStack = pMem;
}
```

##### With error checking

```
void push (StackNode **pStack, char newData)
{
	StackNode *pMem = NULL;

	pMem = (StackNode *) malloc (sizeof(StackNode));

	if (pMem != NULL) {
		// Initialize the dynamic memory
		pMem->data = newData;
		pMem->pNext = NULL;
	}

	// Insert new node onto top of stack
	pMem->pNext = *pStack;
	*pStack = pMem;
}
```

(same as `deleteFront()` in [[Linked Lists]])

### Removing Data from Top of Stack

```
char pop (StackNode **pStack)
{
	StackNode *pTop = NULL;
	char retData = '\0';
	
	if (!isEmpty(*pStack)) {
		pTop = *pStack; // temp storage of top of stack
		retData = (*pStack) -> data;
		*pStack = (*pStack) -> pNext;
		free(pTop);
	}

	return retData;
}
```

(same as `deleteFront()` in [[Linked Lists]])

### Retrieving Data from Top of Stack

```
char peek (StackNode *pStack)
{
	char retData = '\0';
	
	if (!isEmpty(pStack)) {
		retData = pStack->data;
	}
	
	return retData;
}
```

### Applications

- Reversing strings
- Checking for palindromes
- Searching for path in a maze
- Tower of Hanoi
- Evaluating infix expressions
- Function call stacks