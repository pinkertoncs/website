---
title: "Project 01 - Linked Lists"
---

## Description
- This project consists of two(2) classes. The first class, **Person** is used to model, or store information, about a person.  The second class, **List**, is an implementation of a linked list that stores **Person** objects. These classes might be used in a personnel management system.

## Person

- Constructors
    - **Person()** - default constructor
    - **Person(string, string)** - two(2) argument constructor, sets first and last name
- Methods
    - **setName(first, last)** - sets object's first and last name
    - **toString()** - returns a string representation of a Person
    - **compareTo(Person)** compares this Person against the Person parameter
        - returns -1 if this comes before param
        - returns 0 if this and param are equal
        - return 1 if this comes after param
    - Note: first compare by last name, then first name, finally by id (ids are guaranteed to be unique)
- Testing
    - (For the full tests see Main.java and test/PersonTest.java)
    - When you create new instances of a Person, you will invoke the constructors
    - Other methods are invoked using the dot operator (**.**)
```java
// invokes the default constructor, Person()
Person p1 = new Person();

//invokes the 2-arg constructor, Person(String, String)
Person p2 = new Person("John", "Doe");

p1.setName("Jane", "Doe");

// use the toString method for output
System.out.println(p1.toString());

//use the compareTo method, compare p1 and p2
System.out.println(p1.compareTo(p2));
```

## List

- This list is specifically designed to hold Person objects
- Methods (Tier 1)
    - **length()** - returns length of list
    - **toString()** - returns a string representation of this list
    - **push(Person)** - adds a person to the list
    - **pop()** - removes item from the end of list and return reference to popped item
    - **find(Person)** - returns index of param or -1 if not found
    - **get(index)** - return the Person object at index
- Methods (Tier 2)
    - **insert(index, Person)** - insert Person at specified index
    - **pop(index)** - remove Person at index, return reference to popped item
    - **sort()** - sort the list using the Person **compareTo** method

## Main
- The provided **Main.java** has some simple tests for Person and List
- I would recommend commenting out the tests and then un-comment them as they are implemented
- You may modify Main.java as you see fit

## Tips

- **length()**
    - set a *count* variable to 0
    - iterate over the list, incrementing *count*
    - return *count*
- **toString()**
    - create an empty string
    - iterate over the list
        - call the element's toString() method and append it to string
    - return the string
- **push(Person)**
    - create a new node and set it's Person data to the parameter
    - case 1 - adding first element to the list (root is **null**)
        - set root to reference the newly created node
    - case 2 - general case, adding an element to the end of the list
        - iterate to the last node in the list
        - set the newly created node's **next** to null
        - set the last node's **next** to the new node
        - (Doubly Linked List) set the new Node's **prev** to last node
- **pop()**
    - case 1 - empty list
        - return **null**
    - case 2 - single item in list
        - set root to **null** (make sure you keep a reference to the Node)
        - return data
    - case 3 - general case
        - iterate to the last node in the list
        - set the next-to-last node's **next** to null (make sure you keep a
        reference to the last node)
        - return data
