---
tags: CMSC_216
created: 2026-4-30
description: 4/30 notes
---

### Processes vs. Threads

- Processes
	- No memory shared by default
	- Child changes don't affect parent
	- Limited communication by default
	- Limited damage between processes
	- Memory protection between processes
	- Marginally longer startup (`fork()` and `waitpid()`)
- Threads
	- Memory is shared among threads by default
	- Data changes by one thread are visible to all
	- Easy sharing, rich communication possible
	- Unlimited damage between threads
	- No memory protection between threads
	- Marginally faster startup (`pthread_create()` and `_join()`)

### Process and Thread Functions

Threads and processes both represent "flows of control"

|Processes|Threads|Description
|-|-|-
|`fork()`|`pthread_create()`|Create a new flow of control
|`waitpid()`|`pthread_join()`|Get exit status from flow of control
|`getpid()`|`pthread_self()`|Get ID for flow of control
|`exit()`|`pthread_exit()`|Exit (normally) from an existing flow of control
|`abort()`|`pthread_cancel()`|Request abnormal termination of flow of control
|`atexit()`|`pthread_cleanup_push()`|Register function to be called at exit from flow of control

### Thread Creation

```
#include <pthread.h>

int pthread_create(pthread_t *thread,
					const pthread_attr_t *attr
					void *(*start_routine) (void *),
					void *arg);
					
int pthread_join(pthread_t thread, void **retval);
```

- Start a thread running function `start_routine`
- `attr` may be `NULL` for default attributes
- Pass arguments `arg` to the function
- Wait for thread to finish, put return in `retval`