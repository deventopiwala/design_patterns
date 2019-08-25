
# Bridge Design Pattern

**Definition:**

Bridge is a **structural design pattern** that lets you split a large class or
a set of closely related classes into two separate hierarchies (abstraction
and implementation) which can be developed independently of each other.

In short, use composition instead of inheritance, when there are two separate
hierarchies of classes.

**Example:**

TODO: Insert the Before Shape-Circle UML

Gere, shape and color hierarchies are independent, but are varying together.
This creates a cartesian product and causes a class explosion. This also
violates Do not Repeat Yourself (DRY), as circle and square code is repeated.
The red and blue color code is also repeated.

TODO: Insert the After Shapre-Circle UML

As shown in the figure above, we separate out the two hierarachies, which
vary independently. And one of the hierarchy has another object (Composition).

**UML:**

TODO: add the UML here.


**More Concrete Example:**

Consider two types of GUI views; long form and short form views. These display
resources likes artists, books, songs, etc.

TODO: add UML here.

TODO: add reference to the example

View and resources are interfaces. View contains an object of type resource.


**Applicability:**
1. Use the bridge patter when you wan to divide and organize a monolithic class
that has several variants of some functionality.
2. Use this pattern when you want to extend a class in several orthogonal
dimensions. The Bridge suggests that you extract a separate class hierarchy
for each of the dimensions. The original class delegates the related work to
the objects belonging to those hierarchies instead of doing everything on its own.
3. Use the bridge pattern, if you need to be able to switch implementation at
run-time. Althougg, it is optional, the Bridge pattern lets you replace the
implementation object inside the abstraction. It is as easy as assigning a new value
to the field. In our view example, the view takes the instance of a resource. So,
a method in the view class can be added to change the resource at run-time.


**Pros of Bridge:**
1. You can create platform independent classes and applications.
2. The client code works with high level abstractions. It is not exposed to 
platform details.
3. OCP. You can introduce new abstractions and implementations independently
 from each other.
4. SRP. You can focus on high-level logic in the abstraction and on platform detauls
in the implementation.

**Cons of Bridge:**
1. The code might become more complicated. 

