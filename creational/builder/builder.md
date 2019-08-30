# Builder Design Pattern

**Definition:**

Builder is a creational design pattern that lets you construct complex objects
step by step. The pattern allows you to produce different types and respresentations
of an object using the same construction code.

Imagine a complex object that requires laborous step-by-step initialization
of many fields and nested objects. Such initialization code is buried inside
a big constructor with lots of parameters scattered over the client code.
In most cases, most of the parameters will be un-used, making the constructor
call ugly.

The builder pattern suggests that you extract the object construction code
out of the application class and move to a separate class called the builder.

Some of the construction steps might require different implementation when
you need to build various representations of the product. In this case,
you can create several different builder classes that implement the same set
of building steps, but in different manner. Then you can use these builders
in the construction process to produce different kinds of objects.

You can go further and extract a series of calls to the builder steps you
use to construct a product into a separate class called **director**.
The director class defines the order in which to execute the building steps,
while the builder provides the implementation of those steps.

Having a director class is not necessary. You can always call the building
steps in a specific order directly from the client code. However, the director
class might be a good place to put various construction routines so you can
reuse them across your program.

In addition, the director class completely hides the details of prodcut
construction from the client code. The client only needs to assiciate a
builder with a director, launch the construction with the director, and
ge the result from the builder.

**UML:**

TODO: UML

**Applicablity:**

1. Use the builder pattern to get rid of a big constructor.
2. Say you have a constructor with ten optional parameters. Calling such a 
big constructor is very inconvenient; therefor, you overload the constructor
and create several shorter versions with fewer parameters. These constructors
still refer to the main one, passing some default values into omitted
parameters. The builder pattern lets you build objects step by step,
using only those steps that you really need. After implementing the pattern,
you do not have to cram dozens of parameters into the constructor anymore.
3. Use the builder pattern when you want to create different representations
of the same product.
4. Use the builder pattern to construct Composite trees or other complex
objects.

**Pros of Builder:**

1. You can construct objects step by step, defer construction steps or run
steps recursively.
2. SRP. You can isolate complex construction code from the business logic
of your product.

**Cons of Builder:**

1. Increased code complexity.

