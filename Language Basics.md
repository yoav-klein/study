# Variables

## Types of variables:
#### Instance variables (non-static fields):
Objects store their state in these fields. Those are non-static fields, they are special to a <br>
specific object. 

#### Class variables (static fields):
Those are fields that are declared with the `static` keyword. <br>
This tells the compiler that there's exactly one field with this name, <br>
no matter how many instances of this class will be created. <br>
Additionaly, the keyword `final` could be added to indicate that the value <br>
of that field will never change. (like a macro). <br>

#### Local variables:
Variables that are declared inside a method. Local to the specific method. <br>

#### Parameters
That a function takes. <br>


## Naming
The conventions and rules about naming variables in Java are as follows: <br>

- Variables are case sensitive. They may be any length of letters and digits. May begin with a letter, <br> 
a dollar sign ($) or underscore (_), but the convention is to start with a letter. <br>
- The following characters may be letters, digits or underscores (don't use $ at all). <br>
Use full words for you variables, not abbreviations. 
- If the name of your variable is only one word, spell that word all lower-case. <br>
If it consists of more then one word, capitalize the first letter of each subsequent word. <br>
If your variable is a const (final), spell it all uppercase `static final int NUM_GEARS = 6`

## Primitive data types

The Java programming language is statically typed - which means that all variables that are used must be <br>
first declared with a name and type. 
`int gear = 6`
Tells your program that there is a variables named gear that holds a numeric data and has the initial value of 6.
A variable's data type determins the values it may contain plus the opertaions that can be performed on.

The eight primitive values in Java are:
- byte: 8-bit signed integer. It has the minimum value of -128 and maximum 127.
- short: 16-bit signed integer.
- 32-bit signed integer. Since Java SE 8 you can use it for an unsigned integer. 
- long: 64-bit integer. as in int, since Java SE 8 can also be unsigned. 
- float: 32-bit floating point.
- double: 64-bit floating point.
- boolean: true or false.
- char: 16-bit Unicode character.

### Default values

Fields that are declared but not initialized will be set to 0 or null. <br>
Local variables are not initialized by the compiler, you have to set them. <br>

### Literals
You can use literals to assign values directly to your primitives:

```
boolean result = true;
char capitalC = 'C';
byte b = 100;
short s = 10000;
int i = 100000;
```

#### Integer literals
An integer literal is of type long if it ends with l or L.

Integer literals can be expressed with these systems:
- Decimal: base 10.
- Hexa: base 16. 0x
- Binary: base 2. 0b

#### Floating point literal
A floating point literal is of type float if it ends with f or F. Otherwise it is <br>
of type double. 

#### Character and string literals
Character or string literals may contain any Unicode (UTF-16) character. <br>
Always use single quote for char and double quote for string. 

There's also a `null` literal. You can't assign it to primitives. You can do very little <br>
with it, and it is used mostly to indicate that some object is unavailable.

Finally, there's a special type of literal called class literal, formed by taking a type name <br> 
and appending a .class to it. <br>
For example, `String.class`. This refers to the object that represents the class itself.



# Arrays

As in C or C++, an array is a fixed size array of elements.

```

// declares an array of integers
int[] array;

// allocates memory for 10 integers
array = new int[10];

```

The size of the array is not a part of its type. <br>
The declaration alone doesn't create the array. You need to use the _new_ operator. <br>

Another way to create the array, is to use the shortcut syntax:
```
  int[] arr = { 100, 200, 300, 400, 500, 600, 700, 800, 900, 1000 };
```

#### Array of arrays

You can also create an array of arrays, also known as multidimensional array. <br>
This is done by using two (or more) pairs of brackets: e.g.

```
  String[][] names = {
    { "Mr.", "Mrs.", "Ms." },
    { "Smith", "Jones" }
  }
  
  System.out.println(names[0][0] + names[1][0]) // prints "Mr. Smith"
```

In Java, unlike in C, a multidimensional array is an array, who's elements are themselves arrays. <br>
This makes it possible that each array will vary in length.

#### Manipulating arrays
The java.util.Arrays class provides a set of methods to manipulate arrays.

# Operators

#### The type comparison operator _instanceof_ <br>

The operator instanceof allows you to test if an object is of a class type, <br>
or a class that derives from a certain class, or implements a certain interface. <br>

The following program defines a class Parent, an interface MyInterface, <br>
and a class the implements the interface and inherits the superclass. <br>

```
class Parent { }
interface MyInterface { }

class child extends parent implements MyInterface { }

class Program {
  public static void main(String[] args)  {
    Child child = new Child();
    
    System.out.println(child instanceof Parent) // true
    
    System.out.println(child instanceof MyInterace) // true
  }


}
