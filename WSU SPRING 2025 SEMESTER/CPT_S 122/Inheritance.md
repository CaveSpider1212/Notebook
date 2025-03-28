---
tags: CPT_S_122
created: 2025-3-28
description: Lesson 11-1
---

### Introduction to Inheritance in OOP

- Inheritance may be used as a form of *software reuse* or the process of creating new classes from existing classes
- *Inheritance* allows for the implementation of a class that acquires another class's attributes and operations (its capabilities)
	- The class customizes or enhances the capabilities of the acquired class
- *Software reuse* allows for higher levels of developer production through leveraging tested, quality code
- How it works
	- When implementing a new class some data members (attributes) and member functions (operations) might be in common between the new class and an existing class -- the new class could *inherit* the members of the existing class
		- The existing class is referred to as the *base* class (or *superclass*)
		- The new class, which acquires the members, is referred to as the *derived* class (or *subclass*)
			- Represents a more customized or *specialized* version of objects
- The *is-a* relationship represents inheritance
	- Example: if we have an Employee base class and a Manager derived class -- a Manager *is an* Employee but an Employee is not necessarily a manager
- *Has-a* relationships represent *composition*, where an object contains at least 1 object of other classes as members
	- Example: An Employee *has a* "dental plan" (so they have a class DentalPlan attribute) and *has an* "office" (class Office), etc.

### What is Inherited?

- A derived class inherits every member of a base class *except* its:
	- Constructors
	- Destructor
	- Friends
	- Overloaded assignment operator

### Base and Derived Classes

- Base classes tend to be more *general*, while derived classes tend to be more *specific*
- We've established that every derived class is an object of it's base class, so the set of objects representative of the base class is usually *larger* than the set of objects representative of any of its derived classes
	- An Employee class could be representative of all employee types including managers, supervisors, directors, officers, etc.
	- A Manager class is a *smaller*, more *specific* subset of employees

### Protected Members

- The access specifier `protected` provides an intermediate level of protection between `private` and `public`
- Derived classes, and any of its *friends*, have access to `protected` members of a base class, but any *nonmembers* that are *not* friends do not have access

### Forms of Inheritance

##### Single Inheritance

- One derived class inherits from only one base class
- Example: A Manager inherits capabilities of an Employee *only*

```
class Manager : public Employee
{
	// class declarations
};
```

##### Multiple Inheritance

- A derived class inherits from more than one base class
- Example: A TeachingAssistant inherits capabilities of a Worker *and* Student

```
class TeachingAssistant : public Worker, public Student
{
	// class declarations
};
```

##### Multilevel Inheritance

- A derived class acts as a base class for another derived class
- Example: An Officer is created from a Manager and a Manager is created from an Employee
	- An Officer is a type of Manager and a Manager is a type of Employee
- Generally want no more than a few levels

##### Hierarchical Inheritance

- Multiple derived classes inherit from the same base class
- Example: CEO and COO have attributes of an Officer, but also have their own unique attributes

##### Hybrid Inheritance

- Two or more inheritance forms (mentioned above) are combined
- Example: A Chairman inherits from both CEO and COO classes, and CEO and COO inherit from Officer -- forms a diamond relationship

### Accessibility Modes and Inheritance in C++

- `public`, `protected`, and `private`

```
class Manager : public Employee {};

class Manager : protected Employee {};

class Manager : private Employee {};
```

### Advantages and Disadvantages

- Advantages of inheritance
	- Software reuse
	- Reduces code redundancy
	- Reduces code size
	- Promotes readability
	- Promotes extensibility
		- Considers growth of the system -- a system's ability to extend the system with new functionality with minimal changes and impact to the existing system's functionality
- Disadvantages
	- Base classes and derived classes are tightly coupled -- a change to the base class could impact all classes derived from it
	- With a class hierarchy, many data members could remain unused, possibly affecting performance