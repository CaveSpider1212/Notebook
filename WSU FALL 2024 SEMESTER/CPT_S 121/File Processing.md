---
tags: CPT_S_121
created: 2024-09-11
description: Lesson 3.2 - File Processing With Functions
---

- **File stream**: communication channel between a file and a program that enables continuous flow of data

### File Processing Algorithm

**Step 1**: Open the desired file
- Based on file name and permissions (reading, writing, appending)
- Creates a new stream

**Step 2**: Process the file
- Read data from the file
	- Doesn't affect the file
- Write data to the file
	- Completely overwrites existing file
- Add data to the end of the file (append)
	- Retains previous information in the file

**Step 3**: Close the file
- Destroys the stream

### File Functions in C

- To create a file stream, use `FILE *stream` where "stream" is the name of the stream or file variable
- The file functions are located in the "stdio.h" library (must import)
- Open a file:
	- `fopen(stream)` - returns a file handle, and opens a text or data file to the stream given in the arguments ("stream")
- Read from a file:
	- `fscanf(stream, type, &variable)` - inputs the current text from the file stream as the variable type into "variable"
		- For example, `fscanf(inputStream, "%d", &score1)` would input the current line in the file stream called "inputStream", if it's an integer, and put it into the score1 variable
- Write to a file:
	- `fprintf(stream, String, variables)` - outputs the String, which may use some variables that are formatted, into the file stream
- Close a file
	- `fclose(stream)` - closes the file that is opened in the already-created file stream