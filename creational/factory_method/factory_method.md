# Factory Method Pattern

**Definition:**

Factory Method is a creational design pattern that provides an interface
for creating objects in a superclass, but allows sublcasses to alter the
type of objects that will be created.

Also knows as:**Virtual Constructor**

The factory method pattern suggests that you replace direct object construction
calls with the calls to a special factory method. Objects returned by a 
factory method are often referred to as "products".

This change might look pointless. But, consider that there are lots of different
kinds of classes that are of one type and the object creation is parameterized.
The object creation then can be moved to the factory method.

One may also use factory method, if we need to create objects of the same
type, but the object creation varies according to the underlying platform
or operating system.

**UML:**

TODO: UML

**Applicability:**

1. Use the factory method when you do not know beforehand the exact types and
the objects are of same type.
2. The factory method separates product construction code from the code that
actually uses the product. There it is easier to extend the product construction
code independently from the rest of the code.
3. The object creation code could be dynamically changed to change the behavior
of the created products. For example, the factory method creates square buttons.
But, now you need to create round buttons. You could replace the factory method 
object which initially created square buttons, with the one which creates round 
buttons. This can be acheived at run-time.

**Pros of Factory Method:**
1. You avoid tight coupling between the creator and the concrete products.
2. SRP. You can separate the product creation code from the product using
code. And hence, separating out the two concerns.
3. OCP. You can introduce new types of products into the program without
breaking the existing client code.

**Cons of Factory Method:**
1. The code may become complex.