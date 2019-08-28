# Composite Design Pattern

**Definition:**

Composite is a structural design pattern that lets you compose objects into
tree structures and then work with these structures as if they were individual
objects.

Using the composite pattern makes sense only when the core model of your
application can be represented as a tree.

For example, imagine that you have two type of objects: Products and Boxes.
A box can contain several products as well as a number of smaller boxes.
These little boxes can also hold some products or even smaller boxes, and so on.
Say you decide to create an ordering system that uses these classes. Orders
could contain simple products without any wrapping, as well as boxes stuffed
with products and other boxes. How would you determine the total price of
such an order?
You could try a direct approach: unwrap all the boxes, go over all the products
and then calculate the total. This may not be possible, since we would have
2 classes product and boxes. This would make the approach a little difficult,
if not impossible.

Instead, using the composite pattern makes life easier. The composite pattern
suggests that you work with products and boxes through a common interface
which declares a method for calculating the total price.
For a product, the method would simply return the product price. For a box, 
it would go over each item in the box and ask its price, compute the total
and return the total price. If the box in turn contains another box, the
procedure would repeat to get the box price.


**UML:**

TODO: UML


**Practical Example:**

1. Consider a graphics component or a widget. Many graphics components are
containers which contain other graphics components. The graphics components
would inherit from a common widget interface. And may contain a method draw().
The container component's draw method then can draw methods inside the containers,
which in turn can be container components.

2. Another example of of a TODO list application. A todo list may in turn contain
other todo lists. A recursive tree of todo lists.


**Applicability:**

1. Use the composite pattern when you have to implement a tree-like object
structure.

2. The composite pattern provides you with two basic element types that
share a common interface: simple leaves and complex containers. A container
can be composed of both leaves and other containers. This lets you construct
a nested recursive object structure that resembles a tree.


**Pros of Composite:**

1. You can work with complex tree structures more conveniently: use polymorphism
and recursion to your advantage.
2. OCP. You can introduce new element types into the application without
breaking the existing code, which now works with the object tree.


**Cons of Composite:**

1. It might be difficult to provide a common interface for classes whose
functionality differs too mush. In certain scenarios, you would need to
over-generalize the component interface, making it harder to comprehend.




