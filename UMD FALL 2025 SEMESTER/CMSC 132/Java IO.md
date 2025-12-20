---
tags: CMSC_132
created: 2025-11-7
description: Lecture 28 notes
---

### Files

There are two methods of storing data in external files:
- Text files: Stores data in human-readable characters
- Binary files: Contains bytes which represent data in a format specific to a particular program or system

At the low level, all files are stored in binary (0 or 1).

### Input and Output

Text I/O provides a level of abstraction to encode/decode character.

There are several  Java I/O classes in the package `java.io`, which can be categorized by:
- Whether they perform input or output
	- An input object (input stream) reads a stream of data from a file
	- An output object (output stream) writes a stream of data to a file
- Whether they deal with text or binary data
- Whether they're *buffered* (when memory space is temporarily used to store data before it is read to or from I/O devices for efficiency)
- What units of data they operate upon

### The `File` class

- Encapsulates the properties of a file or directory (folder)
- Does not provide methods to read or write data from or to a file
- Some of its methods are:
	- `exists()` tests whether a file or directory exists
	- `delete()` deletes a file or directory
	- `canRead()` tests whether a program is able (has the proper permissions) to read a file

### `InputStream` and `OutputStream`

The `InputStream` class is the (abstract) superclass of all classes representing an input stream of bytes.

The `OutputStream` class is the (abstract) superclass of all classes representing an output stream of bytes.

### Standard Input and Output

- Standard I/O is provided in the `System` class in the `java.lang` package
	- `System.in` (a reference of type `InputStream`) is used for performing standard input
	- `System.out` is used for performing standard output
	- `System.err` is used for performing standard error output

### Character-oriented Text File Classes

- `FileReader`
	- Its `read()` method reads and returns a character, or -1 if the stream has no more data to be read
	- Its `close()` method closes a stream and releases any system resources it's using
- `FileWriter`
	- Its `write(int c)` method writes a single character
	- Its `close()` method closes the stream and releases any system resources it's using

### Buffered Text File Classes

- `BufferedReader`
	- Reads text from a character-input stream, buffering characters for efficiency
	- Its `readLine()` method reads a line of text as a string, and returns a reference to it, or `null` if the stream has no more data to be read
- `BufferedWriter`
	- Writes text to a character-output stream, buffering characters for efficiency
	- `close()`, or normal program termination, *flushes* output buffers

### Formatted Text File Classes

- A `Scanner` breaks input into logical constructs, delimited by whitespace (e.g. integers, floats, strings, etc.)
	- Methods include `hasNext()`, `nextInt()`, `nextDouble()`, `next()`, etc.
	- It can be used with `System.in`
- A `PrintWriter` writes data in terms of logical constructs
	- Some methods are `print()`, `println()`, and `format()`

### Binary File I/O Classes

- Output:
	- A `FileOutputStream` writes bytes to a binary stream
	- A `BufferedOutputStream` causes the output of a binary stream to be buffered
	- A `DataOutputStream` converts primitive type values or strings into bytes and outputs them to a binary stream
- Input:
	- A `FileInputStream` reads bytes from a file
	- A `BufferedInputStream` causes the input of a binary stream to be buffered
	- A `DataInputStream` reads data from a binary stream and converts it into primitive types or strings
- Advantages:
	- Read/write files faster than text files
	- Can store complex data types
- Drawbacks
	- Not human-readable

### Object Serialization

An entire object can be written to an `ObjectOutputStream`, which reads an entire object.