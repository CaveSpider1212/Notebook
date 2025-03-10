---
tags: CPT_S_122
created: 2025-2-24
description: Lesson 6.2
---

### What is a Stream?

- **Stream**: sequence of objects (generally just considered bytes) that flow form a device to memory or from memory to a device
	- For *input* operations, the bytes flow from the device (i.e. keyboard, network connection, disk, etc.) to main meomry
	- For *output* operations, the bytes flow from main menu to the device (screen, printer, etc.)

### Standard Streams in C++

- For *standard* input/output streams, include `<iostream>`
	- `cin` is a predefined *object* of class `istream` and is connected to the standard input device (i.e. keyboard)
		- `cin >> var` uses the stream extraction operator and stops at whitespace for strings
	- `cout` is a predefined *object* of class `ostream` and is connected to the standard output device (i.e. screen)
		- `cout << var` uses the stream insertion operator
- *Member* function `getline()` will read a line from the stream
	- Inserts a null character at the end of the array of characters, removes and discards the '\n' from the stream (i.e. stored as a C string)

### File Streams in C++

- For input/output streams to work with *files*, include `<fstream>`
	- `ifstream` objects enable input from a file
	- `ofstream` objects enable output to a file
	- `fstream` objects for input from and output to a file
- Associate file with a file stream either during construction (applying the constructor) or by calling `open()`
	- `fstream fstr("filename.txt")`
	- `fstr.open("filename.txt")`
- Read from files using:
	- `fstr >> var` - stops at whitespace
	- `fstr.getline()` - read entire line into character array, stored as a C string
- Write to files using:
	- `fstr << var`
- Each file ends with an end-of-file marker (EOF)
	- Check using `fstr.eof()`
- Close a file using `fstr.close()`