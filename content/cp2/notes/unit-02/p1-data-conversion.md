---
title: "Project 01 - Data Conversion"
---

## Objectives

- Use Java Classes
- Use Java int, char, and String data types
- Understand how information is represented in Binary and Hexadecimal formats

## Getting Started

- Your task is to implement the methods of the **Data** class
- The **Data** class
    - stores an integer between **0** and **15** internally (private data member)
    - has methods to get and set values in integer, binary and hexadecimal formats
    - **Constructors**
        - *Data()*
            - creates a new **Data** object without initializing the number
        - *Data(int i)*
            - creates a new **Data** and initialize using the parameter *i*
    - **Setter** methods
        - *setInt(int i)*
            - set value using integer *i*
        - *setBin(string b)*
            - set value using the binary code in string *b*
        - *setHex(char c)*
            - set value using hex character in char *c*
    - **Getter** methods
        - *int getInt()*
            - get value as integer
        - *String getBin()*
            - get values as binary string
        - *char getHex()*
            - get value as hex character
- Starter files
    - **Data.java**
    - **Main.java**
        - program driver & testing
- Note:
    - **Do not** use "brute force" to implement this (i.e. you should **not** have 16 "if" statements in any of the functions)

## Main & Testing

- Your main should have various tests
    1. Simple tests that create instances of **Data** and tests each of the methods
    2. Produce an output table (like the one below), all values should come from the class's methods.

### Main Output
```
Simple tests:
1010
10
B


DEC     HEX     BIN
--      --      --
0       0       0000
1       1       0001
2       2       0010
3       3       0011
4       4       0100
5       5       0101
6       6       0110
7       7       0111
8       8       1000
9       9       1001
10      A       1010
11      B       1011
12      C       1100
13      D       1101
14      E       1110
15      F       1111
```

## Running the tests

- Before submitting your work, please make sure all the supplied test succeed.

![](/images/cp2/unit-02/running_tests.gif)
