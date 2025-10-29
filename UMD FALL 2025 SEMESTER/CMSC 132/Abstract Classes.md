---
tags: CMSC_132
created: 2025-9-15
description: 9/15, 9/17 notes (Lectures 6 and 7)
---

> [!info] `abstract`
> If a method and/or class is `abstract`, then the implementation details are left to the subclasses.
> 
> We need to use abstract methods rather than removing the method completely because if there's a superclass reference to a subclass object, the method must at least be present in the superclass (but doesn't need an implementation) for the code to run without errors (but will call subclass' implementation).

If a class has at least one abstract method, the entire class needs to be abstract.

> [!info]
> Abstract classes can NOT be instantiated as a reference to an object of the abstract class.
> 
> However, if the abstract class has any subclasses, then it CAN be instantiated as a reference to an object of a subclass.

Abstract classes should still have constructors because subclasses can still call them when an object is created (see above), and the abstract class may have fields that need to be initialized.