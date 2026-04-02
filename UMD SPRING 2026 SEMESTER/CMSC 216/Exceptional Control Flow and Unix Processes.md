---
tags: CMSC_216
created: 2026-3-31
description: 3/31 notes
---

### Traditional vs. Modern Computing Devices

Traditional computers had a single executing program which could interact freely with all parts of the computing hardware.

Modern computing devices uses an operating system which manages all programs.

**Operating system** (OS): "Manager" program that coordinates activities of all programs/users, manages hardware and provides abstraction layer, enforces security and fairness

**Process**: A running program with its context

### OS Kernel and Kernel Mode

OS code is usually in the **kernel**, a program that starts running when a computing system is powered on.

- Kernel sets up handlers for various exceptional control flows such as hardware interrupts and system calls
- Most CPUs have (at least) two modes
	- User/Normal mode
	- Kernel/Privileged/Supervisor mode
- User programs run in user mode, cannot directly manipulate hardware or access certain resources
- Requests OS to perform some operations which jumps to kernel code running in kernel mode

### Processes: Running Programs

- Hardware just executes a stream of instructions
- The OS creates the notion of a **process**, a running program and its resources
- Processes can be executed for a while, then paused while another process executes, then continue
- To accomplish this, the OS usually provides:
	- Bookkeeping info for processes (resources)
	- Ability to interrupt/pre-empt a running process to allow OS actions to take place
	- Scheduler that decides which process runs and for how long

### Exceptional Control Flow

- CPUs use "regular" control flow most of the time but support some kinds of **exceptional control flow**
- General idea:
	1. Something triggers exceptional control flow
	2. Normal program instructions pause
	3. Processor jumps to a designated set of instructions to handle the situation
	4. Typical handling code is in the OS Kernel
	5. After the situation is handled control may be returned to the program that was running OR something else may happen
- Exceptional control may include interrupts, traps, faults, aborts, etc.

### Process Context and Context Switches

- Exceptional control flow at the hardware level allows high-level behaviors such as changing between processes
- OS Kernel tracks data structures associated with processes that allows them to be paused and resumed
- **Process context** includes data such as
	- Values of registers as the process is paused
	- Regions of main memory in use by process
	- Open files and other resources in use by process
- Switching between processes is a **context switch**
	- OS saves the context of Process A someplace safe
	- OS loads the context for Process B and starts it running
	- Later A's context can be loaded to resume where it left off

### Exceptional Control Flow Use Cases

- Enable multiple processes to share the CPU
	- OS sets a hardware timer
	- OS selects a process, part of the **scheduler** code in the OS
	- See above section
- Hiding I/O latency
	- Process A requests to receive data from the network
	- OS finds from the Network Interface Card (NIC) that data not available for Process A, so starts Process B and marks Process A as waiting (for I/O to complete)
	- While Process B is running, data arrives to NIC
	- Process A marked as ready to run, scheduler chooses between A and B

### Process Creation/Coordination

`getpid() / getppid()`:
- Get process ID of the currently running process
- Get parent process ID

`wait() / waitpid()`:
- Wait for any child to finish (`wait`)
- Wait for a specific child to finish (`waitpid`)
- Get return status of child

`fork()`:
- Create a child process
- Identical to parent except for return value of `fork` call
- Determines child/parent

`exec()` family:
- Replace currently running process with a different program image
- Process becomes something else losing previous code
- Focus on `execvp()`

