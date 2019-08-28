# Flyweight Design Pattern

**Definition:**

Flyweight is a structural design pattern that lets you fit more objects into
the available RAM by sharing common parts of state between multiple objects
instead of keeping all of the data in each object.

A space optimization technique that lets us use less memory by sharing externally
the data assiciated with similar objects.

A flyweight is an object that minimizes memory usage by sharing as much data
as possible with other similar objects. It is a way to use objects in large
numbers when a simple repeated representation would use an unacceptable 
amount of memory. Often some parts of the object state can be shared, and
it is common practice to hold them in an external data structure (like a map)
and pass them to objects temporarily when they are used.

**UML:**

TODO: UML diagram

**Flyweight Factory:**

For more convenient access to various flyweight obhects, you can create a
factory method that manages a pool of existing flyweight objects. The method
accepts the intrinsic state of the desired flyweight from a client, looks
for an existing flyweight object matching this state, and returns it if it
was found. If not, it creates a new flyweight and adds it to the pool. A hash map
can be used to keepp the existing objects. The hash map acts as a cache for
the flyweight object.

**Practical Example:**

Consider a shooting game, which contains several thousand objects of the same
type. These objects contain sprites/small images. Most of the objects use
the same image. Storing the same image in all the objects will bloat the 
required memory. And hence, these images are re-used. They are stored in the
flyweight. And when needed are passed to the objects as flyweight reference.

**Applicability:**

1. Use the flyweight pattern only when your program must support a huge
number of objects which barely fit into the available RAM and these objects
have a significant shared state.
2. The benefits of applying this pattern depend heavily on how and where it
is used. It is most useful when:

    a. An application needs to spawn a huge number of similar objects.
    
    b. Th objects contain duplicate states which can be extracted and shared
     between multiple objects.
     

**Pros of Flyweight:**

1.  Saves space (RAM), if the application has a large number of similar objects.

**Cons of Flyweight:**

1. As the flyweight object needs to be searched everytime during an operation,
more CPU cycles are required to process the same objects.

2. Code can become more compicated.
