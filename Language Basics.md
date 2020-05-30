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



