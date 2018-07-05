---
title: "Lesson 02 - Lists"
---

## Reference
- Tutorialspoint: [Python Lists](http://tutorialspoint.com/python/python_lists.htm)

## Lists
- A **list** is very similar to a **tuple**, but more flexible
- Define lists using square brackets **[]**
- Use the built-in **len** function to get the length of a list

```python
# create and print list
stuff = [ "bread", "eggs", "milk" ]
print( stuff )

# get length of list
n = len( stuff )
print( "n =",n )
```

### Output
```
['bread', 'eggs', 'milk']
n = 3
```

## Indexing

- Access the list elements using the **index operator []**
    - THE FIRST ELEMENT IS AT INDEX 0
    - Elements can be accessed backwards from the end by using negative indexes

```python
# access elements
first = stuff[0]
second = stuff[1]
third = stuff[2]
print(first, second, third)

# access elements from the back
last = stuff[-1]
print(last)

# get a random element
import random
print( random.choice(a_list))
```

### Output
```
bread eggs milk
milk
eggs
```

## List Reference

- The previous types we have used (**int**, **float**, **string**, **tuple**) are **immutable** types
    - Immutable types cannot be changed
    - when you assign a new variable to an immutable type, the value is copied
- Lists are **mutable**
    - When you assign a new variable to a mutable type, you have a new **reference** to the same object!
- In practice, it looks like this
    - notice that appending to L2 also changed L1
    - L1 and L2 refer to the same object

![](/images/cp1/unit-04/list_reference.png)

```python
# tuples
p1 = (2, 3)
p2 = p1
print( p2 )

# lists
L1 = ['a','b','c']
L2 = L1
L2.append('d')
print(L1)
```

### Output
```
(2, 3)
['a', 'b', 'c', 'd']
```

## Adding and Removing Elements

- List is a class (more on this later), and as such has **methods** (or actions that can be performed on a list)
- **Adding** elements
    - a_list.append(x)
        - add an item to the end of list 'a_list'
    - a_list.extend(L)
        - add multiple items to the end of list 'a_list'
    - a_list.insert(i, x)
        - add an item into list 'a_list' at the given index 'i'
- **Removing** elements
    - a_list.pop()
        - removes and returns last element
    - a_list.pop(i)
        - remove and returns element at index 'i'

```python
print('# setup')
ls = [ "joe", "jane" ]
print( ls )

print('\n# adding elements')
ls.append( "rob" )
ls.extend([ "bill", "phoebe" ])
ls.insert( 2, "marcus" )
print( ls )

print('\n# removing elements')
name = ls.pop(2)
print( "removed: ",name)

print('\n# sorting elements')
ls.sort()
print(ls)
```

### Output
```
# setup
['joe', 'jane']

# adding elements
['joe', 'jane', 'marcus', 'rob', 'bill', 'phoebe']

# removing elements
removed:  marcus

# sorting elements
['bill', 'jane', 'joe', 'phoebe', 'rob']
```

## Counting and Searching

- Inclusion testing
    - Use the **in** operator to check if and item is in a list
- Counting and finding elements
    - a_list.count(x)
        - returns the number occurrences of 'x' in list 'a_list'
    - a_list.index(x)
        - returns the first index of element 'x' in list 'a_list'
    - a_list.remove(x)
        - removes the first element 'x' from list 'a_list'
    - Notes
        - **x in list** has the same truth value as **a_list.count(x) > 0**
        - **index** and **remove** will produce an error if element x does not exist in the list
        - **list.remove(x)** is the same as **list.pop(list.index(x))**

```python
ls = ['joe', 'jane', 'marcus', 'rob', 'bill', 'phoebe']

# remove a found element
x='marcus'
if( x in ls ):
    i = ls.index(x)
    print( "removing element [",x,
        "] at index", i  )
    ls.remove( x )

print( ls )
```

### Output
```
removing element [ marcus ] at index 2
['joe', 'jane', 'rob', 'bill', 'phoebe']
```

## Sorting and Random(ness)

- **Sorting** lists
    - a_list.sort()
        - sort a list in place
    - sorted(a_list)
        - returns a new sorted copy of list
- **Random**(ness) and shuffling
    - random.shuffle(a_list)
        - shuffles list in place
    - random.choice(a_list)
        - returns a random item from the list
    - random.sample(a_list, n)
        - returns a list of n random items from list

```python
import random

x = list('qwertpoiuyasdfglkjhzxcvbnm')
x.sort()
print(x)
random.shuffle(x)
print(x)
print( random.choice(x) )
print( random.sample(x, 5) )
```

## Slicing

- **List slicing** can be used to a copy of a part of a list
    - a[start:end]
        - items from start through end - 1
    - a[start:]
        - items from start through the rest of the list
    - a[:end]
        - items from the beginning through end -1
    - a[:]
        - a copy of the whole list

```python
vowels = list('aeiou')

print(vowels[2:4])
print(vowels[2:])
print(vowels[:4])
print(vowels[:])
```

### Output
```
['i', 'o']
['i', 'o', 'u']
['a', 'e', 'i', 'o']
['a','e','i','o','u']
```

## Nested Lists

- Lists can contain an object type - even lists!
- Lists inside of lists are called **nested lists**

```python
L1 = [1, 2, 3]
L2 = [4, 5, 6]
L3 = [7, 8, 9]
lists = [L1, L2, L3]

print(lists)
print(lists[0])
print(lists[0][0])
```

### Output
```
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
[1, 2, 3]
1
```
