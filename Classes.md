
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






```
```



