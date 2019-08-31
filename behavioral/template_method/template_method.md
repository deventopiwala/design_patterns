# Template Method Design Pattern

**Definition:**

Template method is behavioral design pattern that defines the skeleton of
an algorithm in the superclass but lets subclass override spcific steps of
the algorithm without changing its structure.

The template method suggests that you break down an algorithm into a series
of steps, turn these steps into methods, and put a series of calls to these
methods inside a single "template method". The steps may be abstract or have
some default implementation. To use the algorithm, the client is supposed to
provide its own subclass, implement all the abstract steps, and override some
of the optional ones if needed (but not the template method itself).

**UML:**

TODO: UML

**Applicability:**
1. Use the template method pattern when you want to let clients extend only
particular steps of an algorithm, but not the whole algorithm or its
structure.
2. The template method lets you turn a monolithic algorithm into a serial
of inidividual steps which can be easily extended by subclasses while keeping
intact the structure defined in a superclass.
3. Use the pattern when you have several classes that contain almost identical
algorithms with some minor differences. As a result, you might need to modify
both classes when the algorithm changes.
4. When you turn such an algorithm into a template method, you can also pull
up the steps with similar implementations into a superclass, eliminating
code duplication. The code that varies between the subclasses can remain in
subclasses.

**Pros of Template Method:**

1. You can let clients override only certain parts of a large algorithm, 
making them less affected by changes that happen to other parts of the
algorithm.
2. You can pull duplicate code in the superclass.

**Cons of Template Method:**
1. Some client might be limited by provided skeleton algorithm.

