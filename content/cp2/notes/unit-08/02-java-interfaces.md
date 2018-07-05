---
title: "Lesson 02 - Java Interfaces"
---

## Interfaces & Abstract classes

## References

- [TutorialsPoint](https://www.tutorialspoint.com/java/)
    - "Java Object Oriented" Section
- [Oracle java Doc](http://docs.oracle.com/javase/tutorial/java/IandI/index.html)

## OOP abstraction & encapsulation

- In programming, **abstraction** is the practice of hiding the implementation details of a class behind public methods. This allows a programmer to use a class without knowing how it works, they only need to know what it does.
- Abstraction is closely related to **encapsulation**. We have used this before - by implementing *getter* and *setter* methods rather than accessing a class field directly. This allows you to change the underlying implementation without breaking code.

## Java Abstract class

- A Java **abstract class** is an incomplete parent class. It may contain one or more abstract methods that must be implemented by a derived class
- Abstract class cannot be instantiated - you can not create a new object (instance) from an abstract class
    - In order to create objects, you must create one or more derived classes that implement all of the abstract methods of the parent.

## Java Interfaces

- A Java **interface** is similar to an abstract class, but cannot have any data members, only methods
  - "There are a number of situations in software engineering when it is important for disparate groups of programmers to agree to a **contract** that spells out how their software interacts. Each group should be able to write their code without any knowledge of how the other group's code is written. Generally speaking, interfaces are such contracts." (Oracle)
