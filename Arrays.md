
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
