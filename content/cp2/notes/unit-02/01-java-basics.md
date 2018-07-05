---
title: "Lesson 01 - Java Basics"
---

## Readings

- [Basic Java Syntax](https://www.tutorialspoint.com/java/java_basic_syntax.htm)
- [Basic Data Types](https://www.tutorialspoint.com/java/java_basic_datatypes.htm)
- [Basic Operators](https://www.tutorialspoint.com/java/java_basic_operators.htm)
- [Characters](https://www.tutorialspoint.com/java/java_characters.htm)
- [Strings](https://www.tutorialspoint.com/java/java_strings.htm)
- [File I/O](https://www.tutorialspoint.com/java/java_files_io.htm)

## Primitive Datatypes

- **Primitive types** are the basic, built-in types
- All variables nut be **declared** with their type

    ```java
    int a_number;
    float pi = 3.14;
    ```

- **Initialize variables** by giving then a value or rely on their default **Uninitialized Value**

| Data Type | Default Value | Size |
| :-------: | :-----------: | :--: |
| byte | 0 | 1 Byte |
| short | 0 | 2 Bytes |
| int | 0 | 4 Bytes |
| long | 0L | 8 Bytes |
| float | 0.0f | 4 Bytes |
| double | 0.0d | 8 Bytes |
| char | '\u0000' | 2 Bytes |
| String (or any object) | null | Depends on object |
| boolean | false | Undefined (1 bit) |

### Demo

```java
// declare integer a
int a;

// initialize a
a = 5;

// print a
System.out.println(a);

// declare and initialize float b
float b = 3.14;

// declare and initialize char c
char c = 'A';

// assign char value to int
int d = 'A';

//print d
System.out.println(d);
```

### Output

```
5 // initialized value

65 // ASCII value of character 'A'
```

## Operators

- Virtually identical in use to Python operators. The following are some distinctions
- Increment / decrement (many ways)
- Exponentiation: in the *Math* class

```java
public class Operators{

    public static void main(String[] args) {

        int x = 2;

        // increment 3 times
        x++;
        x += 1;
        x = x + 1;
        System.out.println(x);

        // decrement 3 times
        x--;
        x -= 1;
        x = x - 1;
        System.out.println(x);

        //pow function part of System.Math
        System.out.println(Math.pow(x,3));
    }
}
```

## char & String

- **char**(s) are initialized using single quotes *'* and **String**(s) are initialized using double quotes *"*
- String elements are chars, and are accessible via functions
- String in immutable (just like Python)
- [Java String API](http://docs.oracle.com/javase/8/docs/api/java/lang/String.html)

```java
public class Strings {
    public static void main(String[] args) {
        // chars use single quotes
        char c = 'a';

        //strings use double quotes
        String s = "Hello";

        // accessing a char by string index
        char c2 = s.charAt(0);
        System.out.println(c + " " + s + " " + c2);
    }
}
```

### Output
```
a Hello H
```

## Input & Output
**Notes**
- Input and Output via [PrintStream class](http://docs.oracle.com/javase/8/docs/api/java/io/PrintStream.html)
- Standard input, output, and error PrintStreams are exposed via the [System class](http://docs.oracle.com/javase/8/docs/api/java/lang/System.html)

| PrintStream | System name |
| :---: | :---: |
| input | ```System.in``` |
| output | ```System.out``` |
| error | ```System.err``` |


**Whitespace, Printing**

- printing characters are letters, number, symbols, and whitespace
- **whitespace** includes spaces, tabs, etc
- non-printing characters includes:
    - **newline ('\n')** which a programmer can send to the output stream,
    indicting that the console should insert a line break
    - **carriage return ('\r')** which is inserted into the input stream when
    the user presses the 'enter' key

**Printstream**

- An **output stream** is as it sounds, a stream of symbols that are sent to output
    - **System.out** is the standard output stream, which is printed to the console window
    - **println**, is used to insert data into an output stream
- An **input stream** is a stream of symbols that are collected from input
    - **System.in** is the standard input stream, which is read from the user input in the console.
    - Creating a [Scanner](https://docs.oracle.com/javase/8/docs/api/index.html?java/util/Scanner.html) enables a programmer to read user input from the console

### Demo

```java
import java.util.Scanner;

public class InputOutput {
    public static void main(String[] args) {

        int i;
        char c;
        String s;
        String junk;

        Scanner in = new Scanner(System.in);

        System.out.print( "Hello from stdout!\n" + "Give me an int: ");

        try{
            i = in.nextInt();
            System.out.println("Got " + i );
        } catch(Exception e) {
            // if error, print message and ignore bad number by calling in.next() again
            System.err.println("Could not convert input to integer!");
            in.next();
        }

        System.out.print("Give me a char: ");
        c = in.next().charAt(0);
        System.out.println("Got '" + c + "'");

        System.out.print("Give me a string: ");
        s = in.next();
        System.out.println("Got \"" + s + "\"");

    }
}
```

## Functions

**Review**

- A **function** is a block of code that can be executed on command
    - The function is executed when it is **called / invoked**
- A **function** may have zero, one, or more **parameters**
    - A value passed to a function is called an **argument**
- The **function signature (header)** is the first line with the  visibility, return type,
function name, and list of parameters in parentheses *()*
    - Functions that do not return any data should have the return type **void**
- The **function body** is the block of code after the header, enclosed in curly brackets *{ }*

### Demo
```java
public class Function{

    public static int addition(int a , int b) {
        int r;
        r = a + b;
        return r;
    }


    public static void main(String[] args) {
        int z;
        z = addition (5,3);
        System.out.println("The result is " + z);
    }
}
```
