---
title: "Enrichment 01 -  Sequences and Series"
---

## Directions

- implement the functions defined in *sequences_and_series.py*

## Sample Main Output

```python
sorted: [23, 32, 43, 45, 45, 65, 65, 67, 76, 89]
n: 10
range: 66
sum: 550
mean: 55.0
median: 55.0
mode(s): [45, 65]
---------------------------
arithmetic: [5, 8, 11, 14, 17, 20, 23, 26, 29, 32]
geometric: [2, 4, 8, 16, 32, 64, 128, 256, 512, 1024]
sequence: [-1, 2, -3, 4, -5, 6, -7, 8, -9, 10]
---------------------------
prime: x is prime
primes: [2, 3, 5, 7, 11, 13, 17, 19, 23, 29]
factors: [2, 2, 3, 3]
---------------------------
fibs: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```
## Hints

- Note
    - use these hints only after you've exhausted all other options!
    - These are **definitely** not the only solutions for these problems, and probably not even the best

- **my_range**
    1. sort the list
    2. return the difference between the first and last element

- **my_sum**
    1. initialize a **sum** variable to zero
    2. use a for loop to
        - add a list element to **sum**
    3. return sum

- **mode**
    1. initialize a **max_count** variable to zero
    2. initialize a **modes** list to **[]**
    3. use a for loop to
        - count the frequency (f) of an element (x)
        - if **f** is greater than **max_count**
            - set **max_count** to **f**
            - set **modes** to **[x]**
        - if **f** is equal to **max_count** and **x** is not already in **modes**
            - append **x** to **modes**
    4. return **modes**

- **prime**
    1.  use a for loop to test the divisibility with each number **x** from 2 to (n//2 + 1)
        - if **n** is divisible by **x** ( i.e., the remainder is 0)
            - return False
    2. return True

- **primes**
    1. initialize a **count** variable to zero
    2. initialize a **num** variable to 1
    3. use a while loop to count primes up to the nth
        - increment **num**
        - if **num** is prime
            - increment **count**
    4. return **num**

- **factorize**
    1. initialize and empty list of factors
    2. use a loop to repeat division until **n** is prime
        - use an inner loop to try and divide **n** by **i** from 2 to n // 2
            - if **n** is divisible by **i**
                - append **i** to factors
                - set **n** equals to n // i
                - **break** out of inner loop
    3. return factors

- **fib (without recursion)**
    1. initialize a **fibs** list to [0, 1]
    2. use a loop to find as many values as you need
        - append the new value (sum of previous 2 elements) to **fibs**
    3. return the last element in **fibs**

- **fib (recursive)**
    - base case 1 : if n is 0, return 0
    - base case 2 : if n is 1,return 1
    - recursive case : use the Fibonacci formula
        - Fn = Fn-1 + Fn-2
