# Null Object Design Pattern

**Definition:**

The intent of a Null Object is to encapsulate the absence of an object by
providing a substitutable alternative that offers suitable default do nothing
behavior. In short, a design where "nothing will come of nothing".

**Applicability:**

1. Use the Null Object pattern when some objects should do nothing.
2. Use the Null Object when you want to abstract the handling of null
away from the client.

Given that an object reference may be optionally null, and the result of a
null check is to do nothing or some default value, how can be absence
of an object - the presence of a null reference - be treated transparently?

**Example:**

Consider a screen saver with balls moving on the screen. The balls can have
different colors. The ball colors and movement can be thought of as strategies.
So, a stationary ball with no color is a null strategy. A null strategy object
can be used to provide this behavior. A null movement strategy is to do nothing,
in turn doing nothing does not move the ball.

**UML:**

TODO: UML


A null object can be implemented as a singleton, since the null object basically
contains the same peice of code or absence of code. But, a singleton requires
special handling of code.

**Other Examples:**

1. A null object can be used with the iterator pattern to indicate a non-iterable
object or an empty iterable object.
2. The null object can be used with the command pattern to indicate "no command".
For example, a button when disabled does not have a command or operation.
A no command object can be used here (instead of checking null command.)



