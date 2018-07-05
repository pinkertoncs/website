---
title: "Lesson 01 - Linked Lists"
---

A **linked list**, LL for short, is a type of data structure that can be built from a class
- A linked list is used to store a collection of data
- Advantages over Arrays
    - LL's are dynamically resizable - you can add and remove items at runtime
    - LL's can be reorganized without moving around a lot of data - you just need to change references

An object in a linked list is called a **node**
- Each **node** is an instance of a user-defined class, and holds some data
- A **root reference** points to the first node in the list, called the **root node**
- Each node had a **next reference** that points to the next node in the LL
- The **next** field of the last element is **null**

### Diagram: Simple Linked List
- ![](/images/cp2/unit-04/simple_linked_list.png)

## Defining, creating, and initializing a node

```java
public class SimpleNode {

	public static void main(String[] args) {

    	// create a new node object
    	Node root = new Node();

    	//initialize data member
    	root.name = "Joe";

    	//access data members
    	System.out.println(root.name);

	}
}

//define the node type
class Node {

 	// regular member(s)
 	String name;

 	//link reference(s)
 	Node next;
}
```

### Diagram
- ![](/images/cp2/unit-04/node.png)

## Adding a new node after root
- Just update root's next reference

```java
//define and initialize a new node
Node n = new Node();
n.name = "Jane";
n.next = null;

//add Jane after Joe
root.next = n;
```
### Diagram
- ![](/images/cp2/unit-04/add_node.png)

## Iterating over a Linked List
- To iterate over a linked list define a new node reference to use as a "pointer" to the current node
```java
//can't iterate over empty list
if( root != null ){

    Node iter = root;

    while(iter != null ) {
            // do whatever you need to do with the node
            System.out.println(iter.name);
            iter = iter.next;
    }
    //iter is a reference to the last element in the List
}
```

## Doubly Linked List
- A doubly linked list has a **next** reference and a **prev** reference
- For a 1 element list, these will both be **null**

### Diagram
- ![](/images/cp2/unit-04/doubly-list.png)
