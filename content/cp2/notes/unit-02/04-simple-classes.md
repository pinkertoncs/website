---
title: "Lesson 04 - Simple Classes"
---

## Reading

- [Object Classes](https://www.tutorialspoint.com/java/java_object_classes.htm)

## Introduction

- A **class** is a user-defined data type
- A class is a template used to create **objects**, which are specific instances of the class
- When you define a class, you specify **attributes** (data members) and **methods** (functions) that each instance has
- For example
    - A Rectangle has two attributes: width and height
    - The Rectangle class has methods to set and get the values of those attributes

## Defining and implementing a Class
- Define and implement a java class in it's own **.java** file, i.e. **<Classname>.java**
    - attributes and methods have access or visibility "properties"
        - **public**: accessible where ever the object is in scope
        - **private**: accessible only from within the class itself
    - Methods
        - A **constructor** is called when a class instance is created
        - Since the attributes are private, we need to define methods to set or get their values

## Compiling/Executing a program from the console/terminal
- To compile Java source code into a binary use the **javac** command:

    ```
    javac RunRectangle.java Rectangle.java
    ```

- To run:

    ```
    java RunRectangle
    ```
