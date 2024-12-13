---
tags: CPT_S_121
created: 2024-10-25
description: Lesson 10.1, 10.2, 11.1 - Strutures
---

### Struct Data Type

- `struct` data types are a user-defined type that allow us to combine multiple variables into a single "package" (called "encapsulation")
	- Sometimes referred to as an *aggregate*, where all variables are under one name
	- They can contain multiple different fields (see below)

```
typedef enum {freshman, sophomore, junior, senior} class_t;
typedef enum {anthropology, biology, chemistry, english, compsci} major_t;

// CAN DECLARE A STRUCT LIKE THIS
typedef struct
{
	int id_number;
	class_t class_standing; // see above
	major_t major; // see above
	double gpa;
	int credits_taken;
} student_t;

// WE CAN DEFINE SOME STUDENTS LIKE THIS
student_t student1, student2;
student1.id_num = 123456789;
student1.class_standing = freshman;
student1.major = anthropology;
student1.gpa = 3.5;
student1.credits_taken = 15;

student2.id_num = 987654321;
student2.class_standing = senior;
student2.major = biology;
student2.gpa = 3.2;
student2.credits_taken = 100;

// WE CAN ALSO MAKE A COPY OF A STRUCTURE USING THE ASSIGNMENT OPERATOR
student_t student3 = student1; // each field in student1 is copied to the corresponding field in student3
```

- We use "." to access specific fields of a `struct`
- We can also return structures in functions since they are a data type or use it as a parameter
- If we want to use a structure as an output parameter, we can use the "\*" operator like with pointers (both in the function header and when we are changing the value)
	- We can also use the "->" arrow operator instead to access specific fields of the structure and do the same thing

### Array of Structs

- We can make an array of a `struct` type (in the above example, we could make an array of the `student_t` type)
	- `student_t students[100];`
	- Each item in this array represents one struct

To initialize items in the array, use the dot member operator ("."):
- Set integer, double, etc. types normally with their fields as if it were an array and a structure
	- Example: `students[0].id = 150261372`
- Set strings in the array using `strcpy()`
	- Example: `strcpy(students[0].name, "Joe");`

