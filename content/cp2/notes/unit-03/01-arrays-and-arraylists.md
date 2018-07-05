---
title: "Lesson 01 Arrays and ArrayLists"
---

## Java Array Specification
- [Spec](http://docs.oracle.com/javase/specs/jls/se8/html/jls-10.html#jls-10.7)

## Java Array v.s. Python List

| Java Array | Python List |
| :---- | :---- |
| Single Type | Multiple Types |
| Fixed length | Variable length |
| continuous storage in memory | Highly abstract type |

## Declaring and Initializing Arrays

- You must declare the type and length
- You can initialize all element using a list with braces, but only when you declare the array

```java
int[] foo = new int[5];                // 5 uninitialized integers

int[] bar = new int[]{ 16, 2, 77, 40, 12071 };

//foo = { 1, 2, 3, 4, 5 };         // can't do it.
```

## Arrays in Memory

- A Java Array is a class. It allocates space for the array and a little overhead for Object information
- **Review: Integers & Memory**
    - Recall, an integer on our development platform is 4 bytes (32 bits)
    - When you declare an integer, 4 bytes of memory are reserved and referenced by the variable
    - The variable name provides access to the memory location

- Integer Arrays
    - When you declare an array of integers of size 5, a 20 byte block of memory is reserved (5 ints * 4 bytes)
    - The name of the array (variable) is a reference to the beginning of the block of memory.
- What this means to you, the programmer
    - Since an Java array is a very simple Class (the reference to the array and field containing the size of the array), it doesn't provide the methods of, for example, Python's Lists.  For example, add, remove, etc...

## Iterating over an Array

```java
int[] my_arr = new int[10];

for(int i = 0; i < my_arr.length; i++) {
    my_arr[i] = -1;
}
```

## Multidimensional Arrays

- Sometimes you want to store a tabular data (e.g. multiplication table).  You can use a two-dimensional array for this:

```java
int NUM_ROWS = 3;
int NUM_COLS = 10;

int[][] matrix = new int[NUM_ROWS][NUM_COLS];

for(int row = 0; row < NUM_ROWS; row++) {
    for(int col = 0; col < NUM_COLS; col++) {
        matrix[row][col] = (row+ 1) * (col + 1);
    } //end loop for columns
} //end loop for rows
```

## Passing and Returning Arrays

- Passing

```java
public static void print_array(int[] arr) {

    for(int i = 0; i < arr.length; i++) {
        System.out.println(arr[i]);
    }
}
```

- Returning
    - To "return" an array, you return a reference to the array
     - This example has little practical use, since you must already have access to the array in the calling function.

```java
public static int[] change_array( int[] a ){

    a[0] = 5;
    return a;
}
```

## Java ArrayList API

- [API](http://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html)

## Java ArrayList v.s. Python List

| Java ArrayList | Python List |
| :---- | :---- |
| Single Type | Multiple Types
| Variable length | Variable length |
| Abstract type | Abstract Type |
| add, remove, ... functions | add, remove, ... functions |


## Declaring and Initializing ArrayList

- Optionally, declare a type and/or size

```java
// declare an ArrayList of initial Size 15 that stores Objects
ArrayList aList = new ArrayList(15);

// declare ArrayList with default size that stores
// Integers  (Class wrappers around int)
ArrayList<Integer> iList = new ArrayList<Integer>();
```
## Iterating over and ArrayList

```java
ArrayList<Integer> iList = new ArrayList<Integer>();

for(int i = 0; i < 10; i++) {
    iList.add(-1);
}

for(int i = 0; i < iList.size(); i++) {
    System.out.println(iList.get(i));
}
```

## Passing and Returning ArrayLists

- Passing

```java
public static void print_array(ArrayList<Integer> iList) {
    for(int i = 0; i < iList.size(); i++) {
        System.out.println(iList.get(i));
    }
}
```

- Returning
    - To "return" an ArrayList, you return a reference to the ArrayList
     - This example has little practical use, since you must already have access to the array in the calling function.

```java
public static ArrayList<Integer> change_array( ArrayList<Integer> iList){

    iList.set(0,5);
    return iList;
}
```
