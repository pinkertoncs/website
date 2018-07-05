---
title: "Lesson 03 - Searching and Sorting"
---

## Linear Search

- Start with first element
- Compare each element with search value
- Stop when value is found or end of array is reached


| Advantage | Disadvantage |
| :-----: | :-----: |
| Simplicity | Inefficiency |


## Binary Search

- Require sorted list
- Start in the middle
- if search value < middle element, start over with 1st half
- if search value > middle element, start over with 2nd half
- continue until item is found, or you run out of elements

| Advantage | Disadvantage |
| :-----: | :-----: |
| Efficient | Requires sorted list |

## Sorting Algorithms

- [Sorting Animations](http://www.sorting-algorithms.com/)


## Bubble Sort

- While swap flag is true
    - Set swap flag to false
    - Iterate from first element to next-to-last element
        - if element is greater than subsequent element
            - swap them
            - set swap flag to true

| Advantage | Disadvantage |
| :-----: | :-----: |
| Relatively simple algorithm | Inefficient for large arrays |

## Selection Sort

- Iterate from i=0 to the next-to-last element
    - set least_index to i
    - set least to value at i
    - Iterate from j=(i + 1) to the last element
        - if element is less than least
            - update least_index
            - update least
    - swap the least remaining value to index i

| Advantage |
| :-----: |
|less swapping |

## For Insertion and Merge sort, analyze the animations at the link above
