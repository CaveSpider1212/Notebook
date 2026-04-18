---
tags: CMSC_216
created: 2026-4-9
description: 4/9, 4/14 notes
---

### The Process Table

- OS maintains data on all processes in a **process table**
- Process table entry ~~ process control block
- Contains info like PID, instruction the process is executing, virtual memory address space, and files in use

### File Descriptors

- Each process table entry contains a table of open files
- A use program refers to these via **file descriptors**
- File descriptor is an integer index into Kernel's table
- File descriptor table entry refers to other Kernel/OS data structures

### File Descriptors are Multi-Purpose

- Unix tries to provide most things via files/file descriptor (FD)
- Many Unix system actions area handled via `read()`-from or `write()`-to FDs
- FDs allow interaction with "normal" files to read/change them
- FDs also allow interaction with many other things
	- Pipes for interprocess communication
	- Sockets for network communication
	- Special files to manipulate terminal, audio, graphics, etc.
	- Raw blocks of memory for shared memory communication
	- Even processes themselves have special files in the file system

### Open and Close: File Descriptors for Files

`open()` and `close()` show common features of many system calls.

- Returns -1 on errors
- Show errors using the `perror()` function
- Use of `|` to bitwise-OR several options/flags (write-only, create if needed, etc.) or permissions (user/group read, write, execute)

### `read()` from File Descriptor

`read()`:
- Read up to `SIZE` (defined constant) from an open file descriptor
- Bytes stored in `buffer` (a character array), overwrite it
- Return value is number of bytes read, -1 for error

Caution:
- Bad things happen if `buffer` is actually smaller than `SIZE`
- `read()` does NOT null terminate, so add `\0` manually if needed

### `write()` to File Descriptor

- Write up to `SIZE` bytes to an open file descriptor
- Bytes taken from buffer, leave it intact
- Return value is the number of bytes written, -1 for error

### Standard File Descriptors

When a process is born, it comes with 3 open file descriptors.

|Symbol|\#|`FILE*`|File descriptor for
|-|-|-|-
|`STDIN_FILENO`|0|`stdin`|Standard input (keyboard)
|`STDOUT_FILENO`|1|`stdout`|Standard output (screen)
|`STDERR_FILENO`|2|`stderr`|Standard error (screen)

### Shell I/O Redirection

Shells can direct input/output for programs using `<` and `>`

```
$> some_program > output.txt
# output redirection to output.txt

$> interactive_prog < input.txt
# read from input.txt rather than typing

$> some_program &> everything.txt
# both stdout and stderr to file

$> some_program 2> /dev/null
# stderr silenced, stdout normal
```

### Manipulating the File Descriptor Table

System calls `dup()` and `dup2()` manipulate the file descriptor table.

`int backup_fd = dup(fd)`: Copy a file descriptor to `backup_fd`
`dup2(src_fd, dest_fd)`: Copy `src_fd` to `dest_fd`

### Basic File Statistics

`int ret = stat(file, &statbuf)`: Get statistics on a file `file` and stores it in a `struct stat`, `statbuf`

Attributes like size, file type, permissions, ownership, and time data (some examples) can be accessed from the `struct stat` buffer's fields.

### Movement within Files, Changing Sizes

`int res = lseek(fd, offset, option)`: Move position in file `fd` by `offset` bytes (exact action depends on `option`)

File automatically expands if a position is larger than the current size by filling the holes with 0s (null characters).

`ftruncate(fd, size)`: Set the file `fd` to be `size` bytes big

### Directory Access

Unix file system rooted at `/` (root directory)

Subdirectories like `bin`, `~/home`, and `/home/adhikaab`, for example.

|Shell Command|C function|Effect
|-|-|-
|`mkdir name`|`int ret = mkdir(path, perms)`|Create a directory
|`rmdir name`|`int ret = rmdir(path)`|Remove empty directory
|`cd path`|`int ret = chdir(path)`|Change working directory
|`pwd`|`char *path = getcwd(buf, SIZE)`|Current directory
|`ls`| |List directory contents
| |`DIR *dir = opendir(path)`|Start reading filenames from directory
| |`struct dirent *file = readdir(dir)`|Call in a loop, `NULL` when done
| |`int ret = closedir(dir)`|After `readdir()` returns null