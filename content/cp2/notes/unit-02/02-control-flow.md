---
title: "Lesson 02 - Control Flow"
---

## Readings

- [Java Decision Making](https://www.tutorialspoint.com/java/java_decision_making.htm)
- [Java Loop Control](https://www.tutorialspoint.com/java/java_loop_control.htm)

## Conditional Statements

- Conditional statements in Java have the following syntax differences from Python
    - **The condition must be enclosed in parentheses**
    - If the condition is true, then the subsequent **statement or block** will execute

### Demo
```java
// BASIC condition

Scanner in = new Scanner(System.in);

int x;

x = in.nextInt();

if( x > 0 ){
    System.out.println("x is positive");
} else {
    System.out.println("x is not positive");
}
```

## Comparison Operators

- **Comparable items**
    - numerical types
    - chars (ASCII order)
    - Strings (lexicographically via the **compareTo** method)

| Comparison | operator |
| :--- | :---: |
| less than | < |
| less than or equal to | <= |
| greater than | > |
| greater than or equal to | >= |
| equal to | == |
| not equal | != |

- **Comparing floats**
    - Floating point values are sometimes off by very small amounts
    - When comparing floats, use a margin of error
    - If the absolute value of the difference is below the margin, consider them equal

```java
// returns -1 if a < b,
//	    0 if a==b,
//	    1 if a > b
int flt_cmp( float a, float b ){

    float diff = a-b;

    if(Math.abs(diff) < 0.001)
        return 0;
    else if(diff < 0 )
        return -1;
    else
        return 1;

}
```

## Chaining & Nesting

```java
if( condition1 ){
	//BLOCK1
} else if( condition2 ){
	//BLOCK2
} else if( condition3 ){
	//BLOCK3
} else {
	//CATCH ALL
}
```

```java
if( even ){
	if (prime){
		System.out.println(2);
	}
}
```

## Boolean Expressions

- Can not use natural English words like in Python

| logical operator | operator |
| :----: | :----: |
| and | && |
| or | \|\| |
| not | ! |

- compound comparisons
    - In python is it possible to do a compound comparison with math syntax
    - This is **NOT VALID** in Java

```java
x = 15;

// INCORRECT
if( 0 < x < 10)                       // this will result in a error at compile time
    System.out.println("incorrect");

// CORRECT
if( x > 0 && x < 10 )      // this is the right way to test this
    System.out.println("correct");
```

## Switch Statements

- A **switch statement** is a more compact representation of chained if-else statements. The restriction is that it only does direct comparison (==)

### Demo
```java
switch (x) {
  case 1:
    System.out.println("x is 1");
    break;
  case 2:
    System.out.println("x is 2");
    break;
  default:
    System.out.println("some other value");
  }
  ```

## Looping Statements

## While Loop

- Nearly identical to Python's while loop
- Note that parentheses are required

### Demo
```java
// custom countdown using while
public static void main(String[] args) {

    int n = 10;

    while(n > 0) {
        System.out.println(n);
        --n;
    }

    System.out.println("liftoff!");
}
```

### Output
```
10
9
8
7
6
5
4
3
2
1
liftoff!
```

## For Loop

- Note that ant iteration can be done with a while loop. A for loop is a convenience.
- Java uses **C-style for loops**
    - **for( initialization; condition; step size) { ... }**

### Demo

```java
// countdown using a for loop
public static void main(String[] args) {

    for(int n=10; n > 0; n--) {
        System.out.println(n);
    }

    System.out.println("liftoff!");
}
```

### Multiple statements in loop header

- You can have **multiple** initializations and/or multiple variable changes

### Demo
```java
for ( int n=0, i=100 ; n!=i ; ++n, --i )
{
   // whatever here...
}
```

## Java For-each Loop

- The java For-each loop is similar to Python's **for-in** loop
- The syntax for the for-each loop is
    _ **for( declaration : collection)**
    - where **collection** is any iterable element (more on these later)

### Demo
```java
// range-based for loop
public static void main(String[] args) {
    String str ="Hello!";
    for (char c : str.toCharArray()){
        System.out.print("[" + c + "]");
    }
    System.out.println();
}
```
## Control Statements

- You can use the following control flow statements in a loop
    - **continue**
        - skip the rest of the loop and go to the next iteration
    - **break**
        - exit the loop
