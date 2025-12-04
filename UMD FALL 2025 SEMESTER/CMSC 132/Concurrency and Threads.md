---
tags: CMSC_132
created: 2025-11-19
description: 11/19, 11/21, 11/24, 12/1 notes (Lecture 33, 34, 35, 36)
---

### Processes

A **process** is a program loaded into memory and executing.

Processes have their own independent *address space*, meaning its own region of memory with its own variables and data structures.

Each process may be executing a different program.

If processes need to communicate they can do so via the operating system, files, and the network.

### Threads

A **thread** is a sequentially-executed sequence of instructions inside a process (running concurrently in their process).

Threads share an address space (data) with other threads in the same process.

Each thread has its own execution context, meaning its own runtime stack (local variables).

Threads communicate via shared access to data.

Multiple threads in a process execute the *same* program.

### Multithreading

A **multithreaded** program is one that's written to contain multiple threads that execute concurrently

Motivation:
1. To better utilize hardware resources
	1. When a thread has to wait, the system can do computation for other threads
	2. Given extra hardware, computation for different threads can be done in parallel, which will reduce overall execution time
2. To capture the logical structure of a program
	1. For a program with concurrent interacting components, a thread can be created to handle each one, which simplifies the program

### Creating threads in Java

Two approaches:
1. Extend the `Thread` class
```
public class ThreadedClass extends Thread {}

public class Thread implements Runnable {
	...
}
```
2. Implement the `Runnable` interface (better way)
```
public interface Runnable {
	public void run(); // work for thread
}
```

### Some `Thread` class methods

```
public class Thread implements Runnable {
	public Thread();
	public Thread(Runnable target);
	public void run();
	public void start();
	public static void sleep(long milliseconds);
	public void interrupt();
	public void join();
	public static void yield();
}
```

### Creating threads extending `Thread`

1. Create a class extending `Thread`
2. Put the processing to be performed by the thread objects in the class' `run()` method
3. Create instances (objects) of this class
4. Call `start` on each object (*not* `run()`)

### Creating threads using `Runnable`

1. Create a class implementing `Runnable`
2. Put the processing to be performed by the thread objects in the class' `run()` method
3. Create instances of this "worker" class
4. Create threads to run them, by creating a `Thread` object for each one, passing the worker object to the `Thread` constructor
5. Call `start()` on each thread

`Runnable` is an interface, so it can be implemented by any class, and a class implementing runnable can also implement other interfaces (however, if the class were to extend `Thread` instead, it can't extend other classes, so that's why implementing `Runnable` is better).

### Threads in Java

A thread eventually starts exeucting *only if its `start()` method is called*.

A thread finishes when the `run()` method is finished executing.

The entire threaded program finishes when all threads are finished running.

The *scheduler* (part of the Java Virtual Machine) manages threads, and chooses a waiting thread to run next.

### Thread states

A Java thread can be in one of several states:
- New: It's allocated and is waiting for `start()` to be called for it to run
	- `new()` creates a new thread, putting a thread in this state
- Waiting: It can begin execution
	- Goes to this state when `start()` is called, or when I/O is completed, sleep expires, etc. (why the thread was blocked)
	- Also, `yield()` or time slice can cause a thread from going to the "runnable" to this state
- Runnable: It is currently executing
	- The scheduler has chosen this thread to run
- Blocked: It's waiting for an event (I/O, etc.)
	- I/O, `sleep()`, etc. causes a thread to be in this state
- Terminated: It's finished
	- A thread goes in this state when `run()` terminates

Thread states are defined by an enum `Thread.State` in Java.

When a processing unit (CPU or core) is available and the scheduler chooses a waiting thread to run, this is called *dispatching*.

### Thread scheduling observations

The order threads are selected to run is *indeterminate* - it depends on the scheduler.

Scheduling may not be fair - some threads may execute more often.

A thread can *block* indefinitely (*starvation*) if other threads always execute before it or instead of it.

Note: The `main()` method is also a thread itself.

### Synchronization

**Synchronization** refers to coordination of events between different threads with respect to time.

It may be needed in multithreaded programs to get the results desired.

### The `Thread` class `join()` method

A thread can wait for another one to terminate (which is one form of synchronization) by calling the `join()` method (in the `Thread` class).

`public final void join()`:
- Doesn't return until the thread that it's called on has terminated
- Throws an `InterruptedException` (a checked exception) if interrupted

If you want to run multiple threads concurrently and wait for them all to finish, start the threads first (by calling `start()` on all of them), then join them (call `join()` on all of them).

### Some errors in concurrent programs

A **race condition** is when the order that operations are performed in a concurrent program affects its correctness.

A **data race** is concurrent access by different threads to the same shared variable, where at least one access is a *write*, meaning it modifies the variable.

### Locks

A **lock** is an entity that can be held by only one thread at a time.

Threads can acquire locks and release locks (if they have one).

A thread that tries to acquire a lock that is currently being held by another thread will wait (*block*).

Locks can be used to enforce some types of synchronization by guaranteeing *mutual exclusion*, which refers to limiting the number of threads at a time that can execute some code (usually means allowing only one thread at a time to execute some code).

### Synchronized objects in Java

`synchronized(obj)` allows a thread to acquire the lock for the object `obj`.

```
static final Object o = new Object();
syncrhonized(o) { // acquire lock on o on entry
	... // hold lock on o in block
} // release lock on o on exit
```

If no other thread already has the lock associated with `obj`, the calling thread will acquire it when the synchronized block (the block defined by `synchronized() { ... }`) starts, and release it when it exits the synchronized block.

If another thread does already have the object's lock, the calling thread will wait instead.

Consequently, mutual exclusion is guaranteed for the code in the synchronized block.

A thread releases an object's lock when it leaves the synchronized block for any reason (which could be the end of the block being reached, the block exiting due to a `return`, `continue`, or `break`, or an exception is thrown).

### Critical section

A block of code that only one thread at a time can be allowed to execute, in order to avoid incorrect results (in other words, a block of code that we have to ensure mutual exclusion for), is called a **critical section** (not to be confused with the algorithm complexity analysis term).

Critical sections must be protected (with locks) wherever they appear in a program, otherwise several threads may execute them simultaneously.

### Synchronized methods in Java

`syncrhonized` can be applied to a method, which obtains a lock for execution of its entire body (the lock it gets is for the method's current object).

```
syncrhonized void myMethod() {
	...
}

void myMethod() {
	synchronized(this) {
		...
	}
}

// the above two do the same thing
```

### Synchronization issue #1

Mutual exclusion depends on threads acquiring the *same* lock. There's no synchronization if threads obtain different locks.

### Synchronization issue #2

A sequence of actions may have to be performed atomically to avoid a race condition or data race. The lock must be held for the duration of the transaction.

Local variables are not shared by multiple threads (they are individual per thread).

### Synchronization issue #3

**Deadlock** occurs when a thread holding a lock is unable to obtain a lock held by another thread, and vice versa.

A thread `t` holding a lock can be waiting for an action to be performed by another thread, which is also waiting for `t`'s lock, so the threads are unable to continue execution.

In general, a thread should avoid holding a lock for a long time, and avoid trying to hold more than one lock at the same time.

### Synchronization issue #4

Synchronization incurs runtime overhead, so excessive use will reduce performance.

Only use the minimum synchronization necessary to ensure correct results.

### Common mistakes with threads

If there is a thread object reference `t1` and `t1.sleep(2000)` is called, the `main()` thread is the one that sleeps for two seconds.

If we want to run a thread, we need to call `start()`, NOT `run()`. `run()` is called automatically when a thread is started.

Do not write your own `start()` method. The `Thread` class `start()` method knows how to create a thread, and have it call the `run()` method automatically.

### Thread-safe

Code is considered **thread-safe** if it works correctly when executed by multiple threads concurrently.