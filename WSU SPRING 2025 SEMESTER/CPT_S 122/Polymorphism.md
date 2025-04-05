---
tags: CPT_S_122
created: 2025-4-4
description: Lesson 12-1 and 12-2
---

### What is Polymorphism?

- **Polymorphism**: the ability to use the same expression to denote different operations
	- *Runtime polymorphism* is the ability to associate multiple meanings to a single function name through the use of late or dynamic binding
		- You can process objects of the same class hierarchy as if they are all objects of the hierarchy's *base* class
	- *Compile time polymorphism* is the type that is achieved through function overloading, operator overloading, and templates
- Polymorphism enables you to "program in the general" instead of "program in the specific"
- *Parametric polymorphism* is where the data type is left unspecified and later instantiated, provided by templates
- Allows you to design and implement systems that are *extensible* -- classes can be added with little to no modifications to portions of the program
- `virtual` functions provide a means to apply runtime polymorphism

### Virtual Functions

- Specified using the keyword `virtual`
- **Virtual function**: function whose behavior can be *overridden* or replaced
	- Function *overriding* is a feature that allows a derived class to provide a specific implementation for a function that is provided by a base class -- not the same as function *overloading*

##### Pure Virtual Functions

- Specified by setting the function "= 0" in the declaration
- Does not provide an implementation for the function, just a declaration
- Each derived class must *override* all base class pure `virtual` functions with concrete implementations -- this is not the case for virtual functions that are not pure
- The compiler will report an error if a pure virtual function is not overridden

##### Virtual Destructors

- Required if you need to `delete` an instance of a derived class through a base class pointer
- If the base class destructor is not `virtual`, then trying to delete the derived class object through a base class pointer may result in *undefined* behavior because only the base class destructor will be invoked

##### Abstract Classes

- A class is considered *abstract* if at least one of its `virtual` functions is *pure*
- Cannot be instantiated
- If you have decided that a class must be abstract, then you should make each function that must be overridden pure `virtual`
	- Remember: a "non-pure" virtual function does not have to be overridden!
- Remember classes that can be instantiated are called *concrete classes*

### Hierarchical Inheritance

- If we make a function pure `virtual`, that same function will be sent to different objects through inheritance, and each derived class provides its own implementation for it
	- In the derived classes, the function should have the same return type, name, and parameter list as the base class function, but they do not need to be virtual unless we are overriding them in other derived classes

Importance of virtual functions:
```
Character *pGameChar = NULL; // there is a render() function in Character, the base class

pGameChar = new Alien; // Alien is derived from Character

pGameChar->render(); // if render() was not declared as virtual in the Character class, the program would run the render() function of the pointer's type (Character)
```

Importance of virtual destructors:
```
Character *pGameChar = NULL;

pGameChar = new Alien;

delete pGameChar; // if the base class destructor (~Character()) is not virtual, then the program uses the base class's destructor to delete an Alien, which is bad because the Alien may have attributes that are not in a Character, so it could lead to undefined behavior or memory leaks
```

### Virtual Function Tables

- Polymorphism introduces overhead
	- i.e. more memory consumption and processor time
- The compiler will build a `virtual` function table (vtable) for each class that has at least one virtual function -- each instance of an object of the same class uses the same table
	- An executing program uses the vtable for determining the proper implementation each time a virtual function is called
	- The determination of which function to call at *runtime* denotes *dynamic* binding
- The vtable consists of pointers to each `virtual` function in a class
	- If the function is pure `virtual`, then the function pointer is set to 0 or NULL -- indicates abstract class!
- Three levels of *indirection* required to implement polymorphism
	- First level - the pointers to functions stored in the vtable
	- Second level - when an object of a class with one or more `virtual` functions is instantiated, the compiler inserts in the object a pointer to the associated vtable
	- Third level - pointers to the objects that are declared

### What is Downcasting?

- The compiler provides a means to access derived-class-only members via a base-class pointer that refers to a derived-class object
	- We can explicitly cast the base-class pointer to a derived-class pointer -- this is downcasting

##### Types
Explicit downcast -- C:
```
// Character is the base class, and Alien, Deity, and Human are derived from Character (which have data members mPower, mType, and mGender respectively)

Character *pBase1, *pBase2, *pBase3;
pBase1 = new Deity; // Character * - base-class pointer
pBase2 = new Alien;
pBase3 = new Human;

// below is the only way to access the derived-class members, but it is not type-safe
((Deity *) pBase1)->mType;
((Alien *) pBase2)->mPower;
((Human *) pBase3)->mGender;
```

- Dynamic downcasts safely convert pointers and references to derived-class types in an inheritance hierarchy, allowing for runtime checks, but it only works with *polymorphic* types (meaning it must have at least one virtual function)
	- Done with `dynamic_cast`
	- Returns a value of the new type...if the cast fails, then returns a null pointer

Dynamic downcast -- C++:
```
(dynamic_cast <Deity *> (pBase1))->mType;
(dynamic_cast <Alien *> (pBase2))->mPower;
(dynamic_cast <Human *> (pBase3))->mGender;
```

- Static downcasts are not guaranteed to safely convert pointers and references to derived-class types in an inheritance hierarchy
	- Avoids the cost of a runtime check, but it's only safe if the program has other logic to guarantee that a valid cast can be performed
	- Done with `static cast`