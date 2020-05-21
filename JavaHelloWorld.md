
# Java

*Java platform* contains two components:
- Java Virtual Machine
- Java API

The *JVM* is what runs the compiled *Bytecode*. <br>
The API is a ready-made software components that are ready for use by the programmer. <br>
It's grouped into libraries, called *Packages*, of related classes and interfaces. 


**HelloWorld program** <br>

Save this in HelloWorldApp.java:

```java
/**
*  The HelloWorldApp class implements an application that
* simply prints "Hello World"
*/

class HelloWorldApp {
	public static void main(String[] args)
	{
		System.out.println("Hello World");
	}
}
```

Compile the program:
```shell
$> javac HelloWorldApp.java
```

Run:
```
$> java -cp . HelloWorldApp
```
Notice that when running, you give the name of the Class! If you change the name of the file, it doens't matter. <br>

##### Understanding the program: <br>
There are 3 thing to notice in the above program:
- Comments: we'll leave that for now
- class definition: <br>
In java, each program starts with a class definition.

- Main method: <br>
In Java, every program must contain a main method whose signature is:
`public static void main(String[] args)`

Finally, the `System.out.println` uses the System class from the core library.

