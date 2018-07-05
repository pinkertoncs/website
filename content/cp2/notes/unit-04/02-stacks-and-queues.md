---
title: "Lesson 02 - Stacks and Queues"
---

## Stacks

- Reference
    - [Wikipedia](https://en.wikipedia.org/wiki/Stack_(abstract_data_type))
- A **stack** is a LIFO abstract data type: "Last in, first out"
- Stack Operations
    - **push(item)** adds an item to the top of the stack
    - **pop()** removes an item from the top of the stack
    - ![](/images/cp2/unit-04/stack.png)

## Queues

- Reference
    - [Wikipedia](https://en.wikipedia.org/wiki/Queue_(abstract_data_type))
    - [Priority Queue](https://en.wikipedia.org/wiki/Priority_queue)
- A **queue** is a FIFO abstract data type: "First in, first out"
- Queue operations
    - **enqueue(item)** adds an item to the end of the queue
    - **dequeue()** removes an item from the front of the queue
    - ![](/images/cp2/unit-04/queue.png)

## Priority Queue

- A priority queue adds additional priority information
    - **enqueue(priority, item)** adds an item with a priority
    - **dequeueTop()** removes the item with the highest priority
