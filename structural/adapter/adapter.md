# Adapter Design Pattern

**Definition:**

Adapter is structural design pattern that allows abojects with incompatible
interface to collaborate. Also know as **Wrapper**.

Imagine you are creating a stock market monitoring application. The app
downloads the stock data from multiple sources in XML format and then displays
nice-looking charts and diagrams for the user. At some point, you decice
to improve the app by integrating a small 3rd party analytic library.
But there is a catch: the analytics library only works with data in JSON format.
You could change the library to work with JSON. However, this might break
some of the existing code that relies on the library. And worse, you might not
have access to the library's sources code, making this approach impossible.

The solution is that you create an adapter. This is a special object that
converts the interface of one object so that another object can understand it.
Adapters can not only convert data into various formats, but can also help
objects with different interfacs collaborate.

**UML:**

TODO: UML


**Applicability:**

1. Use the adapter class when you want to use some existing class, but its
interface is not compatible with the rest of your code.
2. The adapter pattern lets you create a middle-layer class that serves as a
translator between your code and a legacy class, a 3rd party class or any
other class with incompatible interface.

**Pros of Adapter:**

1. SRP. You can separate the interface or data conversion code from the 
primary business logic of the program.
2. OCP. You can introduce new types of adapters into the program without
breaking the existing client code, as long as they work with the adapters
through the client interface.

**Cons of Adapter:**

1. The overall complexity of the code increases because you need to introduce
a set of new interfaces and classes. Sometimes it is simpler just to change
the service class so that it matches the rest of your code.


