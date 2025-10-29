---
tags: CMSC_132
created: 2025-10-1
description: 9/26, 9/29 notes (Lectures 11 and 12)
---

An **inner class** is defined in the scope of another class, and can access all fields and methods of the outer class (even if they are private). Likewise, **outer classes** can use private fields of inner class objects and call private inner class methods on them.

```
public class OuterClass {
	private int x;
	
	private class InnerClass {
		private int y;
		void f() {
			x = 1; // accesses OuterClass private field
		}
	}
	
	void g() {
		InnerClass ic = new InnerClass();
		ic.y = 2; // accesses InnerClass private field
	}
}
```

Inner class objects must be instantiated with an object of the enclosing outer class.

Inner classes are useful for private helper classes and being automatically linked to the outer class.

### Using an inner class

Inside an outer class:
```
public class OuterClass {
	private int x = 2;
	
	private class InnerClass {
		private int y = 4;
		
		private int getSum() {
			return x + y;
		}
	}
	
	void doSomething() {
		InnerClass z = new InnerClass();
		System.out.println(z.getSum());
	}
}
```

Outside an outer class:
```
public class OuterClass {
	private int x = 2;
	
	public OuterClass(int xIn) {
		x = xIn;
	}
	
	private class InnerClass {
		private int y = 4;
		
		private int getSum() {
			return x + y;
		}
	}
}

public class SeparateClass {
	public static void main(String[] args) {
		OuterClass b = new OuterClass(2);
		OuterClass.InnerClass a = b.new InnerClass();
		System.out.println(a.getSum());
	}
}
```

Scope:
```
public class OuterClass {
	int x = 2;
	
	private class InnerClass {
		int x = 6;
		
		private void method() {
			int x = 8;
			System.out.println(x); // prints "8"
			System.out.println(this.x); // prints "6"
			System.out.println(OuterClass.this.x); // prints "2"
		}
	}
}
```

### Static nested classes

A **static nested class** is an inner class declared as a static class, which has no link to an instance of the outer class and can only access static fields and methods of the outer class (however it can have nonstatic fields/methods itself).

This is useful if an inner class object doesn't need to be associated with an outer class object, or should survive longer than the outer class object.