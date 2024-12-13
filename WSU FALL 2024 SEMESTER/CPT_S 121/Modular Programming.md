---
tags: CPT_S_121
created: 2024-09-30
---

### Pointers

- **Pointer**: variable that stores its contents as the address of another variable
	- Should be able to use these to access a variable indirectly
	- Allows for modification of the contents of that variable
- We can assign the address of a regular variable to a pointer
```
char *char_ptr = NULL;
int *int_ptr = NULL;

char character = 'A';
int number = 42;

*char_ptr = &character;
*int_ptr = &number;
```

- We can also overwrite the variable the pointer is referencing to
```
*char_ptr = 'B'; // character is now 'B'
*int_ptr = 25; // number is now 25
```

See [[Dynamic Data Structures]] for information on direct and indirect values.

##### Meaning of "*"

- Meaning 1: multiplication (`5 * 3`)
- Meaning 2: "pointer to" (`char *c`)
- Meaning 3: "follow the pointer" (`*i = 4`)
