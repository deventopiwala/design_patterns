# State Design Pattern

**Definition:**

State is a behavioral design pattern that lets an object alter its behavior
when its internal state changes. It appears as if the object changed its
class.
The state pattern is closely related to the concept of **Finite State Machine**.

TODO: add example state machine

The main idea is that, at any given moment, there is a finite number of 
states which a program can be in. Within any unique state, the program
behaves differently, and the program can be switched from one state to 
another instantaneously. However, depending on the current state, the program
may or may not switch to certain other states. These switching rules, caller
transistions, are also finite and predetermined.

State machines are usually implemented with lots of conditional operators
(if or switch) that select the appropriate behavior depending on the current
state of the object. Usually, the state is just a set of values of an object's
field (typically an enum).

The biggest weakness of a state machine based on conditionals reveals itself
once we start adding more and more states and state-dependent behavior to
the class.

The state pattern suggests that you create a new class for all possible states
of an object and extract all state specific behaviors into these classes.

**UML:**

TODO: UML

**Applicability:**

1. Use the state pattern when you have an object that behaves differently
depending on its current state, the number of states is large, and the state
specific code changes frequently.
2. The pattern suggests that you extract all the state specific code into a 
set of distinct classes. As a result, you can add new states or change
existing ones independently of each other, reducing maintenance cost.

**Pros of State:**

1. SRP. Organize the code related to particular states into separate classes.
2. OCP. Introduce new states without changing existing state classes or
the context.
3. Simplify code of the context by eliminating bulky state machine conditionals.

**Cons of State:**

1. Applying the pattern can be an overkill, if a state machine only has a few
states or rarely changes.


