# Iterator Design Pattern

**Definition:**

Iterator is a behavioral design pattern that lets you traverse elements of
a collection without exposing its underlying representation.

Collections are most used data types in programming. Nonetheless, a collection
is just a container for a group of objects.

Most collections store their elements in simple arrays of list. However, 
some of them are based on stacks, trees, graphs and other complex data
structures.
But, no matter how a collection is structured, it must provide a way of
accessing elements so that other code can use these elements. There
should be a way to go through each element of the collection without
accessing the same elements over and over.

This may sound easy, if your collection is based on an array or list. But,
how do you traverse a complex data structure like a tree? One might implement
pre-order traversal or perhaps post-order or in-order traversals.
The client code that works on the collection may not even care how they
are stored. However, since collections provide different ways of accessing
their elements you have no option other than couple your code to the specific
collection class.

The main idea of the iterator pattern is to extract the traversal behavior
of a collection into a separate object called an iterator.

In addition to implementing the algorithm itself, an iterator object encapsulates
all the traversal details, such as the current position and how many elements
are left till the end, etc.

All iterators must implement the same interface. This makes the client code
compatible with any collection type or any traversal algorithm as long as there
is a proper iterator. If you need a special way to traverse a collection,
you just create a new iterator class, without having to change the collection
or the client.


**UML:**

TODO: UML

**Applicability:**

1. Use the iterator pattern when your collection has a complex data structure
under the hood, but you want to hide its complexity from clients.

**Pros of Iterator:**

1. SRP. you can clean up the client code and the collections by extracting
traversal algoritms into a separate class.
2. OCP. you can implement new types of collections and iterators and pass
them to the existing code without breaking anything.
3. You can iterate over the same collection in parallel because each iterator
object contains its own iterator state.
4. You can delay the iterator and continue if and when needed.

**Cons of Iterator:**

1. Using an iterator may be less efficient than going through elements of
some specialized collections directly.

**Practical Examples:**

1. Iterators in C++ STL

