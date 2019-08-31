# Observer Design Pattern

**Definition:**

Observer is a behavioral design pattern that lets you define a subscription
mechanism to notify multiple objects about any events that happen to the
object they are observing

Also know as: **Event-subscriber, listener**

**Example:**

Image that you have two types of objects: a customer and a store. The customer
is interested in a particular brand of product, which should become
available in store very soon. 
The customer could visit (**Poll**) the every day and check the product
availability. But while the product is en-route, most of the trips would
be pointless. On the other hand the store could emails to all customers
each time a product becomes available (**Broadcast**). This could save
some customers from the endless trips to the store. At the same time, it
would upset other customers who are not interested in new products.

The polling mechanism would waste resources in checking for event availability.
And also, if the polling is too slow, it would mean that the event is
received very late or in some cases is lost. In the broadcast method, the 
events will reach the subscribers who are not interested causing them to
check for an unrelated event.

The observer pattern solves this problem allowing subscribers to subscribe
only to those events they are interested in. The publisher then only sends 
the events to the interested subscribers/parties.

The object that has some interesting state is often called as the **subject**,
but since it is also going to notify other objects about the changes to its
state, we will call it **publisher**. All other objects that want to track
the changes to the publishes's state are called **subscribers**.
The observer pattern suggests that you add a subscription mechanism to the
publisher calls so individual objects can **subscribe** or **unsubscribe**
from a publisher.

**UML:**

TODO: UML


**Applicability:**

1. Use the observer pattern when changes to the state of one object may 
require changing other objects, and the actual set of objects is unknown
beforehand or changes dynamically.
2. Use the patter when some objects in your application must observe others,
but only for a limited time or in specific case.

**Pros of Observer:**
1. OCP. You can introduce new subscriber classes without having to change
the publisher's code.
2. You can establish relations between objects at run-time.
