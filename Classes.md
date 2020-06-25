
# Classes
---

## Class declaration

```
class MyClass extends MySuperClass implements MyInterface {
 // consturctors
 // methods
 // fields

}

```

The preceding class is called MyClass, it inherits MySuperClass and implements the MyInterface interface. <br>

In general, a class declaration can include the following components: <br>

1. Modifiers such as *private*, *public*, and others which will be discussed.
2. Class name (initial capitalized by convention)
3. Superclass name, preceded by the _extends_ keyword
4. A list of interfaces that the class implements, preceded by the _implements_ keyword.
5. class body inside { }

## Declaring member variables

There are several kinds of variables:
- Member variables in a class - called fields.
- Variables inside a method or code block - called local variables.
- Parameters passed to a method.

The `Bicycle` class uses the following lines of code to define its fields: <br>

```
public int cadence;
public int gear;
public int speed;
```

Field declarations are composed of three components:
1. Zero or more modifires, such as _public_, _private_
2. Type
3. Name

The fields of class Bicycle are public, meaning they're accessible to any object that can access
the class.

### Access modifiers

The modifier lets you control what classes can access the member fields. For the moment, consider <br> only
private and public.
- private - field is accessible from within the class only.
- public - field is accessible from other classes.

The best practice is to make fields almost always private. 
The access to them is through getters and setters.

## Defining Methods

That's a typical method declaration:
```
public double calculateAnswer(double wingSpan, double length, int numEngines, double grossTons) {
  // do calculation
}
```

Method declarations has six components: <br>

1. Modifiers - public, private, or other.
2. Return type - data type, or void.
3. Name
4. Parameter list
5. Exception list - will be discussed later.
6. Method body.


#### Method Signature
A method signature is consisted of the name and parameters only!


### Method Overloading

Java supports method overloading, meaning - you can have multiple methods <br> 
with the same name and different parameter list.


## Providing Constructors for Your Class

Constructors are used to initialize the class' initial state. They are like ordinary methods <br>, 
except that they don't have a return type:

```
Bicycle(int startCadence, int startSpeed, int startGear) {
  gear = startGear;
  cadence = startCadence;
  speed = startSpeed;
}
```

To create a new Bicycle object, the construcor is called by the `new` operator: <br>
` Bicycle myBike = new Bicycle(30, 0, 8)` <br>

You can overload constuctors also, of course. <br>

You don't have to provide a constructor for your class. If you don't the compiler <br> automatically 
generates one with no arguments. This auto-generated ctor will call <br>
The superclass no-argument ctor, and will complain if the superclass don't have one <br>.

Know that every class inherits from the _object_ class, that does have a no-argument ctor. <br>


## Passing Information to a Method or Constructor

### Parameter types
You can use any type of parameter to pass to a method, <br>
This includes primitives such as int, float, double, etc. <br>
as well as **reference data types** such as objects or arrays. <br>

### Variable Number of Arguments
You can use `varargs` to receive any number of the same type of parameter to a method. <br>

```
public Polygon polygonFrom(Point... corners) {
    int numberOfSides = corners.length;
    double squareOfSide1, lengthOfSide1;
    squareOfSide1 = (corners[1].x - corners[0].x)
                     * (corners[1].x - corners[0].x) 
                     + (corners[1].y - corners[0].y)
                     * (corners[1].y - corners[0].y);
    lengthOfSide1 = Math.sqrt(squareOfSide1);

    // more method body code follows that creates and returns a 
    // polygon connecting the Points
}
```

This is actually like a array. The `corners` argument is treated like an array. <br>

### Parameter names
The only interesting thing here is, that you can have a name of a parameter <br>
which is the same name as a class' field. In this case, the parameter shadows the field. <br>
For example:

```
public class Circle {
    private int x, y, radius;
    public void setOrigin(int x, int y) {
        ...
    }
}
```

any accessing to the variables `x` and `y` in the `setOrigin` function will refer to the <br>
parameters received, not the fields of the class. To refer to the fields, you'll need to use <br>
a qualified name, which will be discussed later. <br>

### Passing primitive data type arguments

Primite data type arguments are passed by value. 

### Passing reference data types

Reference data types parameters, such as objects, are also passed to methods by value. That means that <br>
when the method returns, the passed in reference still references the same object as before. <br>
However, the values of the object's fields can be changed by the method. 

Example: 
```
public void moveCircle(Circle circle, int deltaX, int deltaY) {
    // code to move origin of circle to x+deltaX, y+deltaY
    circle.setX(circle.getX() + deltaX);
    circle.setY(circle.getY() + deltaY);
        
    // code to assign a new reference to circle
    circle = new Circle(0, 0);
}
```

The `moveCircle` method is a method of some arbitrary class, that takes a Circle object and modifies <br>
it's position.  If we invoke that function like this: <br>
`moveCircle(myCircle, 23, 56)` <br>
Then the coordinates of the object that myCircle refers to will change. <br>
In the end of the method, `circle` is assigned with a reference to a new `Circle` object. <br>
This will not persist though, because the reference was passed in by value and cannot be changed. 
