# Memento Design Pattern

**Definition:**

Memento is a behavioral design pattern that lets you save and restore the
previous state of an object without revealing the details of its implementation.

Also know as: **Snapshot**

The memento pattern delegates creating the state snapshots to the actual owner
of that state, the originator object. Hence, instead of other objects trying
to copy the object's state from the outside, the object itself can make 
the snapshot since it has full access to its own state.

The pattern suggests storing the copy of object's state in a special object
called as the memento. The contents of a memento are not accessible to any
other object except the one that produced it. Other objects must communicate
with the memento with a limited interface which may allow finding the metadata
(like the creation time, the name of the performed operation, etc), but not
the object's state contained in the snapshot.

**UML:**

TODO: UML


**Applicability:**

1. Use the memento pattern when you want to produce snapshot of the object's
state and be able to restore the state.
2. The memento pattern lets you make full copies of an objects's state,
including private fields, and store them separately from the object. While
most people remember this pattern thanks to the "undo" use case, it is also
indepensible when dealing with transactions.
3. Use the pattern when direct access to the object's fields/getters/setters
violates encapsulation.
4. The memento makes the object itself responsible for creating a snapshot of
its state. No other object can read the snapshot, making the original object's
state data safe and secure.

**Pros of Memento:**

1. You can produce snapshots of the object's state without violating encapsulation.

**Cons of Memento:**

1. The application may consume lot of memory, if client create memento too often.
This depends on the application and state that has been stored in the memento
object.

 