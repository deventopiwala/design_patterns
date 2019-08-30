# Mediator Design Pattern

**Definition:**

Mediator is a behavioral design pattern that lets you reduce chaotic dependencies
between objects. The pattern restricts direct communication between the 
objects and forces them to collaborate only via a mediator object.

The mediator pattern suggests that you should cease all direct communication
between the components which you want to make independent of each other.
Instead, these components must collaborate indirectly by calling a special
mediator object that redirects the calls to appropriate components. As a
result, the components depend only on a single mediator class, instead of
being coupled to dozens of their colleagues.

**UML:**

TODO: UML

**Applicability:**

1. Use the mediator pattern when it is hard to change some of the classes
because they are tightly coupled to a bunch of other classes.
2. The pattern lets you extract all the relationships between classes into
a separate class, isolating any changes to specific component from the rest
of the components.

**Pros of Mediator:**

1. SRP. You can extract the comminications between the components into a 
single place, making it easier to comprehend and maintain.
2. OCP. You can introduce new mediators without having to change the actual
components.
3. You can reduce coupling between various components.
4. You can reuse individual components more easily.

**Cons of Mediator:**

1. Overtime a mediator can evolve into a god object.

**Practical Example:**

1. Consider a UI dialog box with several widgets/graphics components contained
in the dialog. The UI components then can communicate each other directly
or can communicate via a mediator, in this case the dialog class. Using the
mediator reduces coupling of various UI components and makes it easier to
change individual components without affecting other components in the dialog.


