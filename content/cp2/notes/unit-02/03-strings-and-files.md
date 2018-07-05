---
title: "Lesson 03 - Strings and Files"
---

## String Methods

- String is a Java built-in type
- Strings are immutable (meaning they cannot be changed)
- [Java 8 String API](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)

### Demo
```java
public static void string_methods() {

    String s = "Hello, world!";
    int len = s.length();
    int i;

    // print first and last characters
    System.out.println(s.charAt(0) + " " + s.charAt(len-1));

    //get index of ','
    i = s.indexOf(',');

    // print substring using delimiter ','
    System.out.println(s.substring(0,i));

    //find the first occurrence of "world"
    i = s.indexOf("world");
    System.out.println("First \"world\" at pos " + i);

    //find the next occurrence of "world"
    i = s.indexOf("world", i+5);
    System.out.println("Next \"world\" at pos " + i);
}
```

## Scanner
- The **Scanner** class breaks input into tokens and can parse the tokens into Strings or primitive data types
- [Java 8 Scanner API](http://docs.oracle.com/javase/8/docs/api/java/util/Scanner.html)

### Demo
```java
import java.util.Scanner;

public class StringScanner {
    public static void main(String[] arg) {

        Scanner in = new Scanner(System.in);

        String s = in.nextLine();

        Scanner ss = new Scanner(s);

        String f, l;
        int m;

        try{

            f = ss.next();
            m = ss.nextInt();
            l = ss.next();

            System.out.println(f + " " + m + " " + l );

        }catch(Exception e) {
            System.err.println("something bad happened!");
        }
    }
}
```

## Tokenizing Input

- Tokenizing means separating a line of input into tokens (words) that are separated
by a delimiter
- You can use a **while loop** and a **Scanner**
- Example, tokenizing a line of input without knowing how many items are on the line

```java
import java.util.Scanner;

public class StringTokenizer {
    public static void main(String[] arg) {

        Scanner in = new Scanner(System.in);

        String s = in.nextLine();

        int cnt = 0;
        Scanner ss = new Scanner(s);

        while(ss.hasNext()) {
            String token = ss.next();
            cnt++;
            System.out.println(token);
        }
        System.out.println("processed " + cnt + " tokens.");
    }
}
```

## File I/O

- You can use the **File** and **Scanner** classes to read data from an input file.
- This example will "echo" an input file to standard output

```java
import java.util.Scanner;
import java.io.File;
import java.io.FileNotFoundException;

public class FileReader {
    public static void main(String[] args) {

        //must wrap this code in a try-catch because File may not exist.
        try{

            File f = new File("test.txt");
            Scanner s = new Scanner(f);

            while(s.hasNextLine()) {
                System.out.println(s.nextLine());
            }
        }catch(FileNotFoundException e) {
            System.err.println("File Not Found!");
        }
    }
}
```
