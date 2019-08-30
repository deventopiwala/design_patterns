# Abstract Factory Pattern

**Definition:**

Abstract Factory is a creational pattern that lets you produce families of
related objects without specifying their concrete classes.

In short, abstract factory can be thought of as an aggregation of different
Factory Methods of related objects.

**UML:**

TODO: UML

**Example:**

Consider and application that can be based on light or dark themes. The GUI
elements can be created with light or dark color. We have two abstract factory
objects, one for light and one for dark themes respectively. As there are
two different abstract factory objects (light and dark), the appropriate
object depending on the theme selected, can be used to create the GUI elements.

**Applicability:**

1. Use the abstract factory when your code needs to work with various families
of related products, but you do not want it to depened on the concrete classes
of those products - they might be unknown beforehand or you simply want to
allow for future extensibility.
2. The abstract factory provides you with an interface for creating objects 
from each class of the product family. As long as your code creates objects
via this interface, you do not have to worry about creating the wrong
variant of a product which does not match the products created by your 
application.

**Pros of Abstract Factory:**

1. You can be sure of the products you are getting from an abstract factory
are compatible with each other.
2. You avoid tight coupling between concrete products and client code.
3. SRP. You can separate the product creation code from the product using
code. And hence, separating out the two concerns.
4. OCP. You can introduce new types of products into the program without
breaking the existing client code.

**Cons of Abstract Factory:**

1. The code may become more complicated than it should be, since a lot of
new interfaces and classes are introduced along with the pattern.

