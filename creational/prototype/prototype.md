# Prototype Design Pattern

**Definition:**

Prototype is a creational design pattern that lets you copy existing objects
without making your code dependent on their classes.

Also known as: **Clone**

Say you have an object, and you want to create an exact copy of it. How would
you do it? First, you have to create a new object of the same class. Then you
have to go through all the fields of the original object and copy their values
over to the new object.

But, not all objects can be copied that way. The field may be private and 
not accessible. Sometimes we do not know the class and we rely on the interface
to talk to the class.

The prototype pattern delegates the cloning process to the actual objects
that are being cloned. The pattern declares a common interface for all 
the objects that support cloning. This interface lets clone the object 
without coupling your code to the class. Usually, such an interface contains
the clone method.

**UML:**

TODO: UML

**Applicability:**
1. Use the prototype pattern when your code should not depend on the concrete
classes of objects that you need to copy.

**Pros of Prototype:**
1. You can clone objects without coupling to their client classes.
2. You can produce complex objects by cloning them.

**Cons of Prototype:**
1. Creating complex objects with circular dependencies might be difficult.



**Notes on C++:**

The C++ language provides a mechanism to copy objects via copy constructor
or copy assignment. In these cases, it may not be necessary to provide the
clone method or explicitly implement the prototype pattern.
But, care needs to be taken to explicitly disable copy and assignment operations
when they are not valid. Or else this could lead to problems or memory leaks.

In general, the rule of three must be followed when implementing the copy
semantics.

With the advent on move semantics introduced in C++11, it is important to
implement the rule five (instead of three). Move semantics in C++ allow
efficient "copy", if the source object will no longer be used after the copy.

See:
1. [Rule of three/five/zero](https://en.cppreference.com/w/cpp/language/rule_of_three)
2. [Rule of three/five](https://en.wikipedia.org/wiki/Rule_of_three_(C%2B%2B_programming))

