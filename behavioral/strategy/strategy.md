# Strategy Design Pattern

**Definition:**

Strategy is behavioral design pattern that lets you define a family of 
algorithms, put each of them into a separate class, and make their objects
interchangeable.

The strategy pattern suggests that you take a class that does something
specific in a lot of different ways and extract all of these algorithms
into separate classes called strategies.

The original class, call the context, must have a field for storing a reference
to one of the strategies. The context delegates the work to a linked strategy
object instead of executing on its own. The context is not responsible for
selecting an appropriate algorithm for the job. Instead, the client passes the
desired strategy to the context. In fact, the context does not know much about
the strategies. It works with all strategies through the same generic interface,
which only exposes the method for triggering the algorithm encapsulated
within the selected strategy. This way the context becomes independent of
concrete strategies, so you can add new algorithms or modify existing ones
without changing the code of the context or other strategies.

**UML:**

TODO: UML


**Applicability:**

1. Use the strategy pattern when you want to use different variants of an
algorithm within an object and be able to switch from one algorithm to
another during run-time.
2. Use the strategy pattern to isolate the business logic of a class from the
implementation details of algorithm that may not be as important in the context
of the logic.

**Pros of Strategy:**

1. You can swap algorithms used inside an object at run-time.
2. You can isolate the implementation details of an algorithm from the code
that uses it.
3. You can replace inheritance with compostion.
4. OCP. You can introduce new strategies without having to change the context.

**Cons of Strategy:**
1. Clients must be aware of the various available strategies and differences
between them.
2. If used when only few strategies are required, it may complicate the code.


