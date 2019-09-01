# Chain Of Responsibility Design Pattern

**Definition:**

Chain Of Responsibility (CoR) is a behavioral design pattern that lets you
pass requests along a chain of handlers. Upon receiving a request, each
handler decides either to prcess the request or to pass it to th next 
handler in the chain.

Also know as: **CoR, Chain Of Command**

Consider a privileged operation that needs to be performed by a user. The user
either has read access to the operation or read-write access depending
on the user level. The user can be passed through a chain of handlers to
determine the level of access the user has to that particular operation.

Another scenario is to stop the request handling, when the current handler
is able to handle the request. This scenario is used in GUI system, where
say a click event is propagated to the widgets until it is handled.

The CoR relies on transforming particular behaviors into standalone objects
called handlers. In our case, each check should be extracted into its own
class with a single method that performs the check. The request, along with
its data is passed to this method as an argument.
The pattern suggests you link these handlers into a chain. Each linked handler
has a field for storing a reference to the next handler in the chain. In
addition to processing a request, handlers pass the request further along the
chain. The request travels along the chain until all handlers have had a chance
to process it. A handler can decide not to pass the request further down the 
chain and effectively stop any further processing.

**UML:**

TODO: UML

**Applicability:**

1. Use the CoR pattern when your program is expected to process different 
kinds of requests in various ways, but the exact type of requests and their
sequences are unknown beforehand.
2. Use the pattern when it is essential to execute several handlers in a 
particular order.
3. Use the pattern when the set of handlers and their order are supposed to
change at run-time.

**Pros of CoR:**

1. You can control the order of request handling.
2. SRP. You can decouple classes that invoke operations from classes that
perform the operations.
3. OCP. You can introduce new handlers without breaking existing code.

**Cons of CoR:**

1. If you are not careful, some requests may end up uphandled.
