---
title: "Lesson 01 - Trees and Graphs"
---


## Readings and References

1. [Primary Reference](http://www.tutorialspoint.com/data_structures_algorithms/index.htm)
2. [BST](http://www.algolist.net/Data_structures/Binary_search_tree)

Note: These tutorials are in C++ but the main concepts and graphics apply to Java as well

## Recursion

- Recursion is when a function calls itself!
- In the follow example, we will implement a recursive factorial function
	- **factorial(n)** is defined (for a positive integer) as the product of all integers
    between **1** and **n**
- Consider the following:

``` java
public static int factorial(int n) {
	if( n <= 0 ) {
    	return 0;
    }

    if( n == 1 ) {
    	return 1;
    }

    return n * factorial(n-1);
}
```

- Let's trace the code for **factorial(3)**
	- factorial(3) -> 3 * factorial(2)
    	- factorial(2) -> 2 * factorial(1)
        	- factorial(1) -> 1
- Notice the returns **cascade** back from **factorial(1)** to **factorial(3)**
- Now trace it back:
	- **factorial(3)** -> 3 * 2 * 1
- In our example, the **recursion depth** is 3 because there are 3 calls to factorial
on the call stack before the returns start cascading back

## Trees

- Reference
	- [Tree Data Structure](https://en.wikipedia.org/wiki/Tree_(data_structure))
- A **tree** is a data structure that simulates a hierarchical tree structure
- Terminology
	- A **node** is an item in the tree
    - The **root** of a tree is the top level item
    - An **edge** is a link connecting two nodes
- ![](/images/cp2/unit-05/tree.png)

### Types of Trees

- Reference
	- [Binary Search Tree](https://en.wikipedia.org/wiki/Binary_search_tree)
    - [Trie](https://en.wikipedia.org/wiki/Trie)
- The diagram above depicts a Binary Search Tree. Note, that for any given node, every node
to the left has a lesser value, and every node to the right has a greater value.

### Binary Search Tree Insertion

- This can be done recursively or iteratively
- Recursive solution
	- Note, the first parameter is a reference to a Node
    - In this example, the key and value will be the same number **n**
    - Code (adapted from Wikipedia)

```java

public void insert(int n) {
	root = insertHelp(root, n);
}

public Node insertHelp(Node n, int val) {
	// if n is null
		// create new node to store val, and return new node
	// if val < n's number
		// recurse to the left
	// else
		// recurse to the right
}
```

- In a public method, you won't want to "reveal" the underlying details (namely, the Node reference),
so you will implement a **helper function**
	- In this example, we are assuming that root is a reference to the "root" node of the tree

### Binary Search Tree traversal

- Reference
	- [Wikipedia Tree Traversal](https://en.wikipedia.org/wiki/Tree_traversal)
- **Traversal** is the process of visiting each node in the tree, analogous to iterating over a list
- There are two general ways to traverse a tree
	- Depth first
	- Breadth first

- With depth-first traversal, there are 3 approaches
	- pre-order
	- in-order
	- post-order
- Recursive in-order traversal (pseudo-code)

```
inorder(node)
	if node == null then return
	inorder(node.left)
	visit(node)
	inorder(node.right)
```

### Binary Search Tree removal

- considerably more difficult than the previous operations
- See Deletion section on Wikipedia page for approach


## Graphs

- Reference
	- [Wikipedia Graph](https://en.wikipedia.org/wiki/Graph_(abstract_data_type))
-Terminology
	- vertex
	- edge
- ![](/images/cp2/unit-05/graph.png)
