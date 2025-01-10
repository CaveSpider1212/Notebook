---
tags: CPT_S_122
created: 2025-1-8
description: 1.1
---

### Pointers

```
int num = 3, int *nump = &num;
// address of num is 1000, address of *nump is 2000
```

- Direct value of *num* (num): 3
- Direct value of *\*nump* (nump): 1000
	- This is the address of *num*, the variable *\*nump* is pointing to
- Indirect value of *\*nump*: 
	- This is the direct value of *num*, the variable *\*nump* is pointing to
- Address of *\*nump*: 2000