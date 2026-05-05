---
tags: CMSC_216
created: 2026-4-30
description: 4/30, 5/5 notes
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

### Motivation for Threads

Improve execution efficiency

Assign independent tasks in a program to different threads

1. Parallel execution
	1. Each thread/task computes part of an answer, and then results are combined to form the total solution
	2. Requires multiple CPUs
2. Hide latency of slow tasks
	1. Slow tasks block a thread, but fast tasks can proceed independently allowing program to stay busy while running
	2. Does not require multiple CPUs

### Mutex Locks

Access to shared data must be coordinated among threads.

A **mutex** allows *mutual exclusion*.

Locking a mutex is an *atomic operation*, meaning it is a system call to the OS, it's guaranteed by the OS to complete wholly, and won't interleave with other threads.

Threads will *block* until granted a mutex by the OS.

```
pthread_mutex_t lock;

int main() {
	// Initialize a lock
	pthread_mutex_init(&lock, NULL);
	
	...
	
	// Release lock resources
	pthread_mutex_destroy(&lock);
}

void *thread_work(void *arg) {
	...
	// Block until lock acquired
	pthread_mutex_lock(&lock);
	
	// Do critical stuff here
	...
	
	// Unlock for others
	pthread_mutex_unlock(&lock);
	...
}
```

Since locking/unlocking mutexes is a system call, it takes time for the OS to coordinate threads. Avoiding repeated lock/unlock cycles saves time.