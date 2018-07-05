---
title: "Lesson 02 - Vectors"
---

## References

[Vector API](https://docs.oracle.com/javase/8/docs/api/index.html?java/util/Vector.html)

## Introduction

- The Vector class is an abstract container type like Python lists or Java ArrayLists. You can **add**, **remove** and **insert** elements.
- To use vectors, you must include the vector library

```java
import java.util.Vector;
```

## Declaring Vectors

- When you declare vectors, you must indicate the type you are storing. The syntax is

```java
Vector<type> name = new Vector<>();
```

- The Vector class has other **constructors**

```java
// create a vector with an initial capacity
Vector<Integer> vecA = new Vector<>(5);

// copy the contents of vecA into vecB
Vector<Integer> vecB = new Vector<>(vecA);
```

## Accessing and Modifying members

- You can use the **size()** method to determine how many elements are in the vector.
- Use the **get(index)** method to access elements

```java
Vector<Integer> vecA = new Vector<>(5);

for(int i = 0; i < 5; i++) {
    vecA.add(i);
}

System.out.println(vecA.get(3));
vecA.set(2,3);
System.out.println(vecA);
```

## Looping

- You can use a **for-loop** to access members sequentially

```java
System.out.print("{");
for(int i = 0; i < vecA.size(); i++) {
    System.out.print(vecA.get(i));
    if( i < vecA.size() - 1) {
        System.out.print(", ");
    }
}
System.out.println("}");
```

## Adding and Removing Members

- Use **add(e)** to add an element to the end of the vector
- Use **lastElement()** to access the last member in a vector
- Use **size()** and **remove(index)** to remove the last element in a vector
- *Note: this example demonstrates LIFO (last-in, first-out)*

```java
Vector<Integer> vecA = new Vector<>();

vecA.add(1);
vecA.add(2);
vecA.add(3);

System.out.print("{ ");
while( !vecA.isEmpty()) {

// print last element
 System.out.print(vecA.lastElement());

// remove last element
vecA.remove(vecA.size() - 1);

// same as !vecA.isEmpty()
if( vecA.size() > 0 ){
    System.out.print(", ");
}
System.out.println(" }");
```
