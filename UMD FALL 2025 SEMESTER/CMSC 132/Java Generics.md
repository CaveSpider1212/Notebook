---
tags: CMSC_132
created: 2025-9-22
description: 9/22 notes
---

"**Generic programming**" refers to writing code (or creating data structures) that can be used with different types of data.

Generic programming is done through inheritance or generic type parameters/variables.

### Generic Type Parameters

Generic type parameters/variables are defined using the notation `<X>`, and classes, interfaces, and methods can be parameterized.

Generic type variables provide abstraction over types, and improve readability/robustness.

Example of a generic type parameter in a class:
```
public class MyGeneric<T> {
	private T value;
	
	public void setValue(T v) {
		T tVar;
		
		value = v;
	}
	
	public T getValue() {
		return value;
	}
}
```

We can use generic type parameters as references, method parameters, or method return types.

Note: We can NOT make a new object of a generic type in a generic class (like saying `T value = new T()`)

We can only call methods on a generic parameter type if they are methods in the object class.

Use generic type parameters if you want to use different types in the class.

### Generic Class

Example of using a generic class:
```
MyGeneric<Vehicle> v;
MyGeneric<String> s;
MyGeneric<Integer> i;
```

We can use any type of object or interface inside the `<>`, but we can NOT use primitive types (however we can use wrapper classes instead).

### Bounded Type Parameters

When declaring a generic class you can limit the types that can later be substituted for a type parameter by making it a **bounded type parameter**, as shown below:
```
class MyGeneric2<T extends Vehicle> {
	...
}
```

In the example above, now only types that are `Vehicle` or subclasses of `Vehicle` can be substituted for `T`, and `Vehicle` methods can be called from `T` references in the class.

### Wildcard Type Parameters

The **unbounded wildcard parameter** `?` stands for any unknown type (so `ArrayList<?>` stands for an `ArrayList` whose element type can be anything).

The `?` can be followed by `extends` and a type name, making it a **bounded wildcard parameter** (so `ArrayList <? extends Vehicle>` means an `ArrayList` of any type that is either `Vehicle` or a subclass of `Vehicle`).

The `?` can be followed by `super` (meaning `ArrayList<? super Vehicle>` stands for an `ArrayList` of any type that is either `Vehicle` or a superclass of `Vehicle`).

Wildcard type parameters can be used in reference declarations (and in some cases method return values), but they can't be used when instantiating objects.

One limitation is that you can't add new elements to a data structure with a wildcard type parameter.