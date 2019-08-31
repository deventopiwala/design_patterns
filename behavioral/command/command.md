# Command Design Pattern

**Definition:**

Command is a behavioral design pattern that turns a request into a standalone
object that contains all information about the request. This transformation
lets you parameterize methods with different requests, delay or queue a
request's execution, and support undoable operations.

Also know as: **Action, Transaction**

**Example:**

Consider a GUI element Button. To invoke an action one may customize the
button behavior using inheritance.

This approach works, but as the application grows there will be a class
explosion of Button classes. So, if something changes in the base Button
class, the change may then propagate to the derived classes. This would
a maintenance headache.

Also, the functionality implemented by the derived button might be required
elsewhere. For example, one could save by pressing the save button, or by
pressing ctrl-s or via the menu item. The code would then be duplicated
across these classes.

Once could use the following solution. The solution separates the concerns,
the GUI and business logic in separate classes.

TODO: draw the before/after diagrams

An UpdateCommand interface class can be implemented, which all the three
classes implement and the same object can be passed to these classes to
achieve the functionality.

**UML:**

TODO: UML


**Applicability:**

1. Use the command pattern when you want to parameterize objects with operations.
2. The command can turn into a specific method call into a standalone object.
3. USe the command pattern when you want to queue operations, schedule their
execution, or exeucte them remotely.
4. Use the command pattern when you want to implement reversible operations.
Although, there are many ways to implement the undo/redo behavior, the command
patterns is perhaps the most popular. To be able to revert operations, you need
to implement the history of performed operations. The command history is
a stack that contains all executed command objects along with related backups
of the application's state.

This method has two drawbacks:

1. It is not easy to save an application's state because some of it can be
private. This problem can be mitigated with the Memento pattern.
2. The state backups may consume quite a lot of memory. Therefore, sometimes
you can resort to an alternative implementation: instead of restoring the 
past state, the command performs the reverse operation. The reverse operation
also has a price: it may turn out to be hard or even impossible to implement.

**Pros of Command:**

1. SRP. You can decouple classes that invoke operations from classes that
perform these operations.
2. OCP. you can introduce new commands to the application without breaking
existing client code.
3. You can implement undo/redo operations.
4. You can implement deferred exeuction of operations.
5. You can assemble a set of simple commands into a complex one.

**Cons of Command:**

1. The code may become complicated since you are introducing a new layer 
between the senders and receivers.

 
