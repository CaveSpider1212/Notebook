---
tags: CMSC_132
created: 2025-9-11
description: 9/8, 9/10 notes
---

Define new class from existing oneusing `extends`.

Subclass inherits fields and methods from superclass, but can also define new fields and methods of their own.

Inheritance facilitates and promotes code reuse because rewriting fields/methods already in the superclass in the subclass is not needed.

Subclass follows "is-a" relationship with superclass

> [!info] Calling Superclass Constructor
> Implicitly calls the superclass' no-argument constructor so that all of the subclass' fields (which they inherited from the superclass) will have a value defined by default.
> 
> If the superclass no-argument constructor is missing, there will be an error.
> 
> Can call superclass constructor explicitly using `super()` (must be at the top of the subclass constructor).
> 
> Regardless of implicit or explicit, the superclass constructor is always called before subclass constructor.

### Polymorphism

Superclass reference can refer to both superclass and subclass objects (but this isn't true the other way around)
--> This is because subclass objects already are superclass objects.

"\[reference] `instanceof` \[class-name]" tests if a reference is an *instance* of a class (whether directly of that class or a subclass of that class).

"\[reference].`getClass()`" returns the exact class the reference is a part of, and can be compared using `.equals()` or `==`, etc. (comparison only returns true when the exact classes are the same; subclasses do NOT count).

However, they are bad design.

> [!info]
> Superclass references can NOT access the fields and methods exclusive to the subclass even if it is referring to the subclass object

> [!info] Casting
> **Downcasting**: Superclass object --> subclass type
> 
> Downcasting only valid when superclass reference refers to subclass object.
> 
> **Upcasting**: Subclass object --> superclass type
> 
> Always valid since a subclass object is already a superclass object.

> [!info] Method Overriding
> Instead of `instanceof` or `getClass()`, best to use **method overriding**, where a subclass redefines methods in a superclass (the overridden method takes precedence over the original superclass version).
> 
> The type of object the method is called on determine which method is called (NOT the type of reference).
> --> This decision is made during runtime, called dynamic method binding.
> 
> Note: Static methods can NOT be overridden