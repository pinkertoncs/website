---
title: "Lesson 03 - Loops and Iteration"
---

## References

- Tutorialspoint [Python Loops](http://www.tutorialspoint.com/python/python_loops.htm)

## Print with end

- When you use the print function, you can specify the end character using the named parameter **end**
    - by default, the last character is a **line break \\n**
    - for more info about special characters, revisit the I/O Notes from Unit 2
- If you want to print just a line break, you can call **print** with no parameters

```python
print( "joe" )
print( "bob", end="." )
print( "jane" )
print()               # extra line break
print( "billy", "jess" )
```

### Output
```
joe
bob.jane

billy jess
```

## While loops

- while loops are conditionals that execute repeatedly for as long as the condition is True.
    - In the example below, the **loop body** (indented) will be executed 10 times

```python
x=0
while( x < 10 ):
    print(x, end=',')
    x += 1
print()
```
### Output
```
0,1,2,3,4,5,6,7,8,9,
```

## For loops

- **for-loop with range**
    - header syntax: **for x in range(...):**
    - x assumes each value in the range
    - the body is executed once for each value in the range
- The **range** function generates a sequence of numbers
    - range(stop)
        - 0 to stop - 1
    - range(start, stop)
        - start to stop -1
    - range(start, stop, step)
        - 0 to stop - 1 with given step

```python
for x in range(10):
    print(x, end=',')
print()

for x in range(5,10):
    print(x, end=',')
print()

for x in range(0,10,2):
    print(x, end=',')
print()
```

### Output
```
0,1,2,3,4,5,6,7,8,9,
5,6,7,8,9,
0,2,4,6,8,
```

## List iteration
- **Iterating over a list** is going through the elements, one at a time
- A **for-loop** is used to iterate
    - Like a function, a for-loop has a header and a body
    - The header has syntax: **for x in L**
    - The variable *x* assumes each value in list *L*, one at a time
    - The body is executed once for each element
- You can also **iterate with the index** using the range function

```python
vowels = ['a','e','i','o','u']

# method1
for letter in vowels:
    print(letter, end=',')
print()

# method2
n = len(vowels)
for index in range(n):
    print( vowels[index], end='-' )
print()
```

### Output
```
a,e,i,o,u,
a-e-i-o-u-
```

## Loop control

- The **break** keyword will exit a loop early
- The **continue** keyword will skip to the next iteration

```python
for char in "python":
    if char == 'y':
        continue

    if char == 'o':
        break

    print( char, end='')
```

### Output
```
pth
```

## Building lists

- You can use a loop to generate a list, like so
    - Start with an empty list
    - append items as you go
- *Note: be careful about generating large list, you could end up using a lot of memory!*

```python
numbers=[]
for x in range(10):
    numbers.append(x)

print(numbers)
```

### Output
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

## Nested loops

- You can use nesting to repeat loops
- The code in the body of the **outer loop (for i ...)** will execute 5 times total
- the code in the body of the **inner loop (for j ...)** will execute 25 times total - 5 times for each run of the outer loop
- Study the example below
    - note the use of the **tab character: \\t**

```python
rows = 5
cols = 5

for i in range(rows):
    print( i, end=':\t')
    for j in range(cols):
        print( j, end='\t')
    print()
```

## Output
```
0:    0    1    2    3    4
1:    0    1    2    3    4
2:    0    1    2    3    4
3:    0    1    2    3    4
4:    0    1    2    3    4
```

## Generators

- Python's **range** function is actually a **generator**
- A generator acts like a list, but
    - it does not hold everything in memory at once
    - you can only access the items sequentially using the **next** function
- You can use a generator with for loops
- You can cast a generator to a list type

```python
# implementation of range function
def numbers(n):
    x=0
    while(x<n):
        yield x
        x += 1

# access using next
g = numbers(3)
print(next(g))
print(next(g))
print(next(g))

# access using loop
for x in numbers(10):
    print(x, end='-')
print()

# cast to list
print(list(numbers(5)))
```

### Output
```
0
1
2
0-1-2-3-4-5-6-7-8-9-
[0, 1, 2, 3, 4]
```

## Recursion

- **Recursion** is when a function calls itself!
    - recursion can be used to loop

```python
def recurse(n):

    # base case:
    if(n==0):
        return

    # do stuff
    print(n, end=', ')

    # call recurse with the next #
    recurse(n-1)

recurse(10)
```

### Output
```
10, 9, 8, 7, 6, 5, 4, 3, 2, 1,
```
