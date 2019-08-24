
# Decorator Design Pattern

**Definition:**

Decorator is a **structural design pattern** that lets you attach new behavior
to the objects by placing these objects inside special wrapper objects that 
contain the behavior.

A decorator object wraps the behavior of another decorator objects.
The wrapper object and the object being wrapped are of same type.

TODO: Insert the donut diagram here.

**Notes:**

Furthermore, there can be any number of decorator objects wrapped inside one another.

The base object (the first one to be wrapped) can be thought of as a base
case in a recursion. The processing of the decorator stops once the base object is processed.

**UML:** 

TODO: Insert UML here.

**Types of Decorators:**
1. Dynamic Decorator

The Dynamic decorator is the same as the normal decorator.

Source Example:
 
```
struct shape
{
    virtual string str() = 0 ;
} ;
struct circle : shape
{
    virtual string str() { return "circle" ; }
} ;

//decorator class
struct colored_shape : shape
{
    colored_shapre( shape &s_ , string &color_ )
    : s{ s_ } , color{ color_ }
    {
    }
    virtual string str()
    {
        return s.str() + " is of color" + color ;
    }
    shape   s ;
    string  color ;
} ;
int main()
{
    circle  c ;
    coloured_circle red_circle{ c , "red" } ;
    cout << red_circle.str() << endl ;
    return 0 ;
}
```
Output:
> circle is of red color

2. Static Decorator:

Source Example:
```
struct circle
{
    string str()    { return "circle" ; }
} ;
template <typename T>
struct colored_circle : T
{
    colored_circle( string &color_ )
    : color{ color_ }
    {
    }
    string str()
    {
        return T::str() + " is of color" + color ;
    }
    string color ;
} ;
int main()
{
    circle  c ;
    colored_circle<circle>  red_circle{ "red" } ;
    cout << red_circle.str() << endl ;
    return 0 ;
}
```
Output:
> circle is of red color

**Applicability:**

1. Use the decorator pattern when you need to be able to assign extra behavior
to objects at run-time without breaking the code that uses the object.
2. The decorator lets you structure your business logic into layers, create 
a decorator for each layer and compose objects with various combinations
of this logic at run-time. The client code can treat all these objects
in the same way, since they all follow the same interface.
3. Use the pattern when it is not possible to extend the behavior using inheritance.
4. Many programming languages have the final keyword that prevents extension of
classes. For these classes, the only way to reuse the existing behavior
is to use the decorator pattern.

**Pros of the Decorator pattern**

1. You can extend the object's behavior without making new subclasses.
2. You can add or remove responsibilities from the object at run-time.
3. You can create several beahviors by wrapping an object into multiple decorators.

**Cons of the Decorator pattern:**

1. The initial configuration of the objects might get complicated.

**Another Example:**

1. Consider a pizza cost calculating class. A pizza can be of different types.
Lets consider, that the cheese pizza is the base pizza and all other pizzas
are built on the cheese pizza. So, we create a class with cheese pizza
and then have decorators with other pizza types (say, Italian or meat-lovers) .
[Source of example](https://www.youtube.com/watch?v=j40kRwSm4VE)

2. Similar situation applies to coffes. A latte can be plain, and then
vanilla and caramel lattes can be built from the plain latte.
[Source of example](https://www.youtube.com/watch?v=GCraGHx6gso)





