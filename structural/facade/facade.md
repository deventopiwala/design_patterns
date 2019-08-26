# Facade Design Pattern

**Definition**

Facade is a structural design pattern that provides a simplified interface
to a library, framework, or any other complex set of classes.

Image that you must make your code work with a broad set of objects that
belong to a sophisticated library or framework. Ordinarily, you would
need to initialize all of those objects, keep track of dependencies,
execute methods in the correct order and so on. As a result, the business
logic of your application/class would become tightly coupled to the implementation
details of the complex library/class, making ti hard to comprehend and maintain.

A facade provides a simple interface to a complex subsystem which contains
lots of moving parts. A facade might provide limited functionality in
comparison to working with the subsystem directly. However, it includes
only those features that clients really care about.

**UML:**

TODO: add UML

**Applicability:**

1. Use the facade pattern when you need to have a limited but straight forward
interface to a complex system.
2. Often, subsystems get more complex over time. Sometimes applying design
patterns leads to increase in number of classes. Although, the subsystem
may become more flexible and easier to reuse in various contexts, but
the amount of configuration and boiler plate code it demands from the clients
grows even larger. The facade attempts to fix this problem by providing a shortcut
to the most used features of the subsystem which fit the client requirements the most.
3. Use the facade when you want to structure a subsystem into layers.
4. Create facades to define entry points to each level of a subsystem.
You can reduce coupling between multiple subsystems by requiring them to
communicate only through facades.

**Pros of Facade:**
1. You can isolate your code from the complexity of a subsystem


**Cons of Facade:**
1. A facade can become a god object coupled to many classes in the system.
