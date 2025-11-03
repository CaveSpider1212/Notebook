---
tags: CMSC_132
created: 2025-11-3
description: 10/22, 10/31 notes (Lectures 21, 25)
---

> [!info] The Iterator Design Pattern
> Definition: Move through a collection of objects without knowing its internal representation
> 
> Where to use and benefits:
> - Use a standard interface to represent data objects
> - Allows changing how a class stores data without other classes that are using it (iterating over the data) having to change
> - Allows easily substituting one class for another (as long as both implement the pattern)
> 
> Need to distinguish variations in the traversal of an aggregate.

^3e6c80

> [!info] The Factory Pattern
> Definition: Provides an abstraction for deciding which class should be instantiated based on parameters given
> 
> Where to use and benefits:
> - A class cannot anticipate which subclasses must be created
> - Separate a family of objects using shared interface
> - Hide concrete classes from the client
> 
> Example:
> ```
> class Ferrari implements Car { ... } // fast car
> class Bentley implements Car { ... } // antique car
> class Ford implements Car { ... } // family car
> 
> Car fast = new Ferrari(); // returns fast car
> 
> public class CarFactory {
> 	public static Car create(String type) {
> 		if (type.equals("fast")) {
> 			return new Ferrari();
> 		}
> 		else {
> 			if (type.equals("antique")) {
> 				return new Bentley();
> 			}
> 			else {
> 				if (type.equals("family")) {
> 					return new Ford();
> 				}
> 			}
> 		}
> 	}
> }
> 
> Car fast = CarFactory.create("fast");
> ```

> [!info] The Decorator Pattern
> Definition: Attach additional responsibilities or functionality to an object
> 
> Where to use and benefits:
> - Provide flexible alternative to subclassing
> - Add new function to an object without affecting other objects
> - Make responsibilities easily added and removed dynamically and transparently to the object

> [!info] The Marker Interface Pattern
> Definition: Label semantic attributes of a class
> 
> Where to use and benefits:
> - Need to indicate attribute(s) of a class
> - Allows identification of attributes of objects without assuming they are instances of any particular class