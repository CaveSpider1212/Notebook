---
tags: CPT_S_122
created: 2025-3-10
description: Lesson 8.2
---

### Class Scope and Accessing Class Members Explored Further

- A class's data members (attributes) and member functions (operations) belong to the *class's scope*
- Nonmember functions do not belong to any class's scope; they are *global* namespace scope
- Within a class's scope data members are directly accessible by the member functions
- Outside of the class's scope, public members are accessed through one of three different handles:
	- An object *name*, a *reference* to an object, or a *pointer* to an object
	- Note: the "this" pointer is considered an implicit handle available only within an object
- Local variables declared inside of a member function have *block* scope

### Access and Utility Functions

- **Access function**: a function that can read or display data
	- **Predicate function**: access function that tests a condition and returns true or false; generally append "is" to the front of the function name
		- isEmpty(), isFull(), etc.
- **Utility function**: private member function used to support other member functions' operations
	- Also called *helper* functions

### Container Classes

- Classes designed to hold and organize a collection of other classes
	- Examples of *sequence* containers include: lists, vectors, etc.
	- Examples of container *adapters* include: stacks, queues, etc.
		- Container adapters are adaptations or interfaces designed to restrict functionality for an already existing container -- they provide a different set of functionality
		- The Standard Template Library (STL) stack and queue adapt the double-ended queue
- Container classes are generally separated into four categories:
	- Sequence containers: represent *linear* data structures
		- Array, double-ended queue, doubly-linked list, vector, forward_list
	- Container adapters
	- Ordered associative containers: represent *nonlinear ordered* data structures
		- Set, multiset, map, multimap
	- Unordered associative containers: represent *nonlinear unordered* data structures

### Properties of STL Sequence Containers

- <u>Array</u>: fixed size; direct access to any element
- <u>Double-ended queue</u>: rapid insertions and deletions at front or back; direct access to any element
- <u>List</u>: doubly linked list; rapid insertions and deletions anywhere
- <u>Vector</u>: rapid insertions and deletions at back; direct access to any element
- <u>Forward_list</u>: singly linked list; rapid insertions and deletions anywhere; C++ 11

### Properties of STL Container Adapters

- <u>Stack</u>: last-in, first out (LIFO)
- <u>Queue</u>: first-in, first out (FIFO)
- <u>Priority_queue</u>: highest priority element is always the first one out

### Functions common to Container Classes

- **Default constructor**: initializes an *empty* container
- **Copy constructor**: initializes the container to be a *copy* of an *existing* container of the same type
- **Move constructor**: *moves* the contents of an existing container into a new container of the same type without copying each element of the argument container
- **Destructor**: performs house keeping or *cleanup* when container is no longer needed
- **Empty**: returns *true* if there are no elements in the container; *false* otherwise
- **Insert**: *inserts* an item into the container
- **Size**: returns the number of elements in the container
- **Copy operator (=)**: copies the elements of one container into another container of the same type
- **Move operator (=)**: *moves* the contents of one container into another without copying each element of the argument container
- **Max_size**: returns the *maximum* number of elements for a container
- **Begin**: *overloaded* to return an *iterator* that refers to the *first* element of the container
- **End**: *overloaded* to return an *iterator* that refers to the *next* position after the *end* of the container
- **Erase**: *removes* one or more elements from the container
- **Clear**: *removes all* elements from the container

### Iterators

- Similar properties to a *pointer*
- An *iterator* is any object that points to some element in a sequence of elements, and has the ability to iterate through the elements using ++ and indirection (\*) operators
- *Containers* support the use of iterators

### Class Templates

- We have already seen function templates, we will now extend the idea to classes
- *Class templates* allow for a way to easily specify a variety of related overloaded functions (*function-template specializations*) or classes (*class-template specializations*)
- Allow for *generic* programming
- Keyword `template` denotes the start of a class template
- STL containers are "templated"