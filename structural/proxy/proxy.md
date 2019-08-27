# Proxy Design Pattern

**Definition:**

Proxy is a structural design pattern that lets you provide a substitute
or placeholder for another object. A proxy contracts the access to the
original object, allowing you to perform something either before or after
the requests gets through to the original object.

Why would you want to control access to an object? Here's an example: you
have a massive object that consumes a vast amout of system resources. You
need it from time to time, but not always. You could implement lazy
initialization: create this object only when its actually needed. All of
the object's clients would need to execute some deferred initialization code.
Unfortunately, this would probably cause a lot of code duplication. In an
ideal worl, we would want to put this code directly into our object's class
but that isn't always possible. For example, the class may be a part of a
closed third party library.

The proxy patten suggests that you create a new proxy class with the same
interface as the original service object. Then you update your application
so that it passes the proxy object to all of the original object's clients.
Upon receiving a request from a client, the proxy creates a real service
object and delegates all work to it.

**UML:**

TODO: add UML


**Applicability:**

There are many ways to utilize the proxy pattern.

**Types of Proxies:**

**1. Lazy Initialization (Virtual Proxy):**

This is when you have a heavy weight service object that wastes system 
resources by being always up, even though you only need it from time to
time.
Instead of creating the object when the application launches, you can delay
the object's initialization to a time when it's really needed.


**2. Access Control (Protection Proxy):**

This is when you only want specific clients to be able to use the service
object; for example, when you objects are crucial parts of an operating system
and clients are various launched applications. The proxy can pass the request
to the service object only if the client's credentials mtach some criteria.

**3. Remote Proxy:**

Local execution of a remote service (remote proxy). This is when the service
object is located on the remote server. In this case, the proxy passes the client
request over the network, handling all the nasty details of working with the network.

**4. Logging Proxy:**

This is when you want to keep a history of requests to the service object.
The proxy can log each request before passing it to the service.

**5. Caching Proxy:**

This is when you need to cache results of client requests and manage life cycle
of this cache, especially if results are large. The proxy can implement caching
can implement caching for recurring requests that always yeild the same results.
The proxy may use the parameters of requests as the cache keys.

**6. Smart References:**

This is when you need to be able to dismiss a heavy weight object once there
are no clients that use it. The proxy can keep track of clients that obtained
a reference to the service object or its result. From time to time, the proxy
may go over the clients and check whether they are still active. If the client
list gets empty, the proxy might dismiss the service object and free the
underlying system resources.
The proxy can also track whether the client had modified the service object.
Then the unchanged objects may be reused by other clients. (Smart pointes in C++)

**Pros of Proxy:**
1. You can control the service object without clients knowing about it.
2. You can manage the lifecycle of the service object when cleints do not
care about it.
3. The proxy works even if the service object is not available or ready.
4. OCP. You can introduce new proxies without changing the service or clients.

**Cons of Proxy:**
1. Code may get more complicated.
2. The response from teh service might get delayed.





