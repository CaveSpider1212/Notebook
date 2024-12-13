---
tags: CPT_S_121
created: 2024-10-18
description: Lesson 9.2 - Strings
---

- **String**: sequence of characters terminated by the null character ('\0')
	- Accessed via a pointer to the first character in it
	- Represented as an array of characters, must account for the extra null character

```
// Declaring strings

char name[20] = "Bill Gates";
char *name = "Bill Gates";
char name[] = ['B', 'i', 'l', 'l', ' ', 'G', 'a', 't', 'e', 's', '\0'];

// they all do the same thing
```

- Storing a string literal into a pointer will place it in memory where the string can't be modified, but placing it in a character array does allow it to be modified

- When using `scanf(%s, array)`, the program will keep reading the string until a white space is encountered
	- Also, there is no & sign required since the array is already an address
- Use `gets(array)` to read a complete line, including the white spaces, until the enter key is pressed, and store it into "array," and use `puts(array)` to display a string followed by a new line

### Array of Strings

- Created using a 2D array, with the number of rows being the max number of strings and the number of columns being the max length of each string including the null character

```
char names[10][20]; // creates an array of up to 10 strings, each with a max length of 20 characters including white spaces and the null character
```

### \<string.h> Functions

- `strlen(char *str)`: returns the length of a string `str`
	- `strnlen(char *str, maxLen)` returns the length of a string `str` up to `maxLen` bytes of the string
- `strcpy(char *dest, char *src)`: copies the source string `src` to the destination string `dest`
	- `strncpy(char *dest, char *src, maxLen)` copies at most `maxLen` bytes of the source string to the destination string
- `strcat(char *dest, char *src)`: appends a copy of the source string `src` to the end of the destination string `dest`, and the terminating character of the destination is replaced with the first character of the source
	- `strncat(char *dest, char *src, maxLen)` appends at most `maxLen` bytes of the source string to the end of the destination string
- `strcmp(char *str1, char *str2)`: compares 2 strings `str1` and `str2` based on their ASCII values (returns 0 if they are equal, a negative number if `str1` is less than `str2`, and a positive number if `str1` is greater than `str2`)
	- `strncmp(char *str1, char *str2, maxLen)` compares at most `maxLen` bytes of the strings

The "n" functions are useful if the string might not have the null/terminating character at the end, so we specify the number of bytes instead.

### \<ctype.h> Functions

In the following functions, we pass a character as the argument in the functions, but the program actually passes the corresponding ASCII value into the function instead. This is why the function headers have an `int` in them but "character" in the description.

- `isalpha(int c)`: checks if a character `c` is an alphabetic character (returns a positive number if it is, returns 0 if it isn't)
- `isdigit(int c)`: checks if a character `c` is a numeric character (returns a positive number if it is, returns 0 if it isn't)
- `islower(int c)`: checks if a character `c` is a lowercase character (returns a positive number if it is, returns 0 if not)
- `isupper(int c)`: checks if a character `c` is an uppercase character (returns a positive number if it is, returns 0 if not)
- `toupper(int c)`: if a character `c` is a lowercase character, return the character as an uppercase character (otherwise returns the same character)
- `tolower(int c)`: if a character `c` is an uppercase character, return the character as a lowercase character (otherwise return the same character)
- `ispunct(int c)`: checks if a character `c` is a punctuation character (returns a positive number if it is, returns 0 if not)
- `isspace(int c)`: checks if a character `c` is a white-space character, such as a space, new line, tab, etc. (returns a positive number if it is, returns 0 if not)
- `isalnum(int c)`: checks if a character `c` is an alphanumeric character, meaning either an alphabet or a digit (returns 1 if it is, returns 0 if it isn't)