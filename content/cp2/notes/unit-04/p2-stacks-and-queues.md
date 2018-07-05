---
title: "Project 02 - Stacks and Queues"
---


## Stack

1. implement the Stack Abstract Data Type using the built-in Java ArrayList class.

2. Use your stack to implement a postfix expression evaluator

- Postfix algorithm
	- Starting at the beginning of the expression, get one term (operator or operand) at a time
		- If the term is an operand, push it onto the stack
		- If the term is an operator, pop two operands off the stack, perform the operation, and push the result back onto the stack
	- hen you get to the end of the expression, there should be exactly one operand left on the stack. That operand is the result.

### Example

```
56 47 + 2 *
```

### Output
```
286
```

## Queue

1. Implement the Queue Abstract Data Type using the built-in Java ArrayList class
2. Implement a restaurant queue
	1. Customers at a restaurant can place their order in the sequence in which they arrive.
	2. The restaurant staff staff can process order concurrently, it takes 2 minutes from the start of processing one order to the next
	3. Each customer's orders takes a certain amount of time to fulfill.
3. I/O queue
	1. Input: a list of customers with the processing time for their order
	2. Output: a list of the order in which the customer are served and the time (from t=0 at the start) at which they will be served.
	3. If two customer's orders are ready at the same time, the customer who arrived first should be served first

### Example

```
joe 13
moe 5
jane 7
may 5
```

### Output
```
serving moe at 7
serving jane at 11
serving may at 11
serving jow at 13
```
