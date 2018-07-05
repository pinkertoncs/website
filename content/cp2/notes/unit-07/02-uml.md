---
title: "Lesson 02 - Unified Modeling Language"
---

## References

- [Agilemodeling UML Class Diagrams](http://www.agilemodeling.com/artifacts/classDiagram.htm)
- [IBM UML basics: The class diagram](http://www.ibm.com/developerworks/rational/library/content/RationalEdge/sep04/bell/)

## UML Tools

- Use [lucidchart](https://www.lucidchart.com/) or [draw.io](https://www.draw.io/) for your design diagrams
- **Lucidchart Setup**
    - Sign in with your Pinkerton account and select free account
    - In Account settings, go to [Google Drive Integration](https://www.lucidchart.com/users/googleDrive) and select "*Automatically sync documents I create in Lucidchart to my Drive account*" to create a Lucidchart folder in your Google Drive
    - When you create a new document, choose **UML** under **Categories**
- **Draw.io Setup**
    - Login with your Pinkerton account

## Modeling classes

- Create your classes in Lucidchart (or draw.io)
- Each class has 3 sections: ClassName, fields (attributes), and Methods.
    - Fields should have a +/- for public/private, name, type, and default value (if any)
    - Methods should have +/-, name, parameters (if any), and return

![](/images/cp2/unit-07/uml-class.png)

## Object associations

- **Association (USES)**
    - Objects interact in some way
    - "A user drives a car"
    - **Directionality**: Associations are typically bidirectional (each object knows about the other object), but are sometimes unidirectional (you can use an arrow to indicate directionality)
    - **Multiplicity**: Associations often indicate multiplicity (how many).  In the example below, a user can drive zero or more (0..*) cars, and a car can be driven by zero or more users.

![](/images/cp2/unit-07/uml-association.png)

## Aggregation & Composition

- **Aggregation (HAS-A)**
    - One Object is a part of another, but the part can exists independently
    - "A car has an engine - but the engine can exist without the car"

![](/images/cp2/unit-07/uml-aggregation.png)

- **Composition (OWNS)**
    - One object is part of another, and its existence is dependent
    - "A house has a room - the room cannot exist without the house."

![](/images/cp2/unit-07/uml-composition.png)

# Inheritance

- **Inheritance (IS-A)**
    - child is a type of parent
    - "A car is a type of vehicle"

![](/images/cp2/unit-07/uml-inheritance.png)
