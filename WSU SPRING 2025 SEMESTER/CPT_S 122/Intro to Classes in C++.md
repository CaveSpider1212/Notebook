---
tags: CPT_S_122
created: 2025-2-12
description: Lesson 5.2
---

### Function Templates

- Overloaded functions are defined to perform similar operations that involve different types and/or program logic
- Function templates can be used to concisely overload functions
	- Done if the program logic and operations are identical for each type

```
// must be in header (.hpp) file
template <class T>
T add(T v1, T v2)
{
	T result = v1 + v2;
	return result;
}

// start of .cpp file
int main(void)
{
	int n1 = 10, n2 = 20, n3 = 0;
	double d1 = 35.75, d2 = 45.5, d3 = 0.0;
	
	// C++ generates overloaded functions for integers and doubles
	n3 = add(n1, n2); // 30
	d3 = add(d1, d2); // 81.25
}
```

### Classes w/ Member Functions

- Classes control access to its members (making them private or public)
- Typically you can't call a *member function* unless an object of the class has been instantiated
	- Exception: declaring member function with the `static` keyword
- Classes allow the developer to separate *interfaces* from *implementation*, which is a principle of good software engineering
	- Generally place function prototypes for member functions in the header (.hpp) file and implementation of these in the source (.cpp) file
	- The function prototypes describe the classes public interfaces without exposing the internal implementation of the member functions
- Objects can interact with each other by sending *messages*
	- *Messages* are sent from one object to another by calling a method on that object, which are generally public member functions

### Constructors for Initializing Objects

- Each class declared provides a *constructor* that may be used to *initialize* an object
- A *constructor* is a special member function because it MUST be named the same as the class, it cannot return a value, and it is called *implicitly* when an object is instantiated
- If a class does not *explicitly* provide a constructor, then the compiler provides a *default* constructor (with no parameters)
- Constructors are usually `public`
- When is an object instantiated?
	- When a variable of the type of class is declared
	- When the `new` operator is explicitly invoked (`new` replaces `malloc()`)
- We often need to overload our constructor with different parameters

### The Rule of Three

- **Rule of Three**: if one or more of the following are defined, then all three should be explicitly defined
	- Copy constructor
	- Destructor
	- Copy assignment operator

##### Copy Constructor

- **Copy constructor**: make a *copy* of an object of the same type
- Always accepts a parameter, which is a reference to an object of the same class type
	- Example: `ComplexNumber (ComplexNumber &copyObject);`
- A copy constructor is *implicitly* invoked when an object is *passed-by-value*
- A *shallow* copy is made if only the data members are copied directly over to the object
- A *deep* copy is made if new memory is allocated for each of the data members

##### Destructors

- Each class declared provides a *destructor*
- Must be named the same as the class with a tilde (~) in front
	- Example: `~ComplexNumber();`
- Called implicitly when an object is destroyed
- If a class does not explicitly provide a destructor, then the compiler provides an "empty" destructor
- When does an object get destroyed?
	- When the object leaves scope
	- When the `delete` operator is explicitly invoked (`delete` replaces `free()`)

##### Copy Assignment Operator

- Overloading the `=` operator
- Copies each field in the right side of the `=` operator into the object it is referring to (the one on the left side)

### Setters and Getters

- These are `public` interfaces/functions to provide access to `private` data members
- **Setters**: allow *clients* of an object to *set* or modify the data members
	- *Clients* include any statement that calls the object's member functions from *outside* the object
	- May be used to *validate* data
- **Getters**: allow client to obtain/*get a copy* of the data members
- There generally should be 1 setter function per data member, and 1 getter function per data member