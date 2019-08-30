# Singleton Design Pattern

**Definition:**

Singleton is a creational design pattern that lets you ensure that a class
has only one instrance, while providing a global access point to this instance.

The singleton pattern solves two problems at the same time, violating the SRP.
1. Ensure that the class has only one instance. For example, we have a shared
resource like a database or a file and we want to control the access to it.
2. Provide a global access point to that instance.

**UML:**

TODO: UML

**Applicability:**

1. Use the singleton pattern when a class in your program should have just
a single instance available to all clients. For example, access to a single
shared database.
2. Use the singleton pattern when you need stricter control over global variables.

**Pros of Singleton:**

1. You can be sure that the class has only one instance.
2. You gain a global access point to that instance.
3. The singleton object is initialized only when it is requested for the
first time.

**Cons of Singleton:**

1. SRP. Singleton violates the SRP, it solves two problems at a time.
2. The pattern requires special treatment in a multi-threaded environment
so that multiple threads would not create a singleton object several time.
3. It may be difficult to unit test the client code of the singleton because
many test frameworks rely on inheritance when producing when producing mock
objects. Since the constructor of the singleton class is private and overriding
static methods is not possible in most languages, you will need to think
of creative ways to mock the singleton.


**Practical Examples:**

1. Use singleton for a shared resource like a database.
2. Use singleton control a single hardware device like the watchdog timer.


