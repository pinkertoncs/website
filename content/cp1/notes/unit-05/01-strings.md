---
title: "Lesson 01 - Strings"
---

## References

- Tutorialspoint: [Python Strings](http://www.tutorialspoint.com/python/python_strings.htm)
- Wikibooks: [Python Programming / Strings](https://en.wikibooks.org/wiki/Python_Programming/Strings)

## String Basics
- Strings work just like lists of characters

```python
# make reference to string
s = "Kulik"

# basics: printing, length, indexing
print(s)
print(len(s))
print(s[0], s[-1])

# iterating
for letter in s:
    print(letter, end='.')
print()


# iterating with index
for i in range(len(s)):
    print(s[i], end='-')
print()
```

### Output
```
Kulik
5
K k
K.u.l.i.k.
K-u-l-i-k-
```

## String slicing
- Use slicing to get a part of string
- works just like list slicing (see notes)

```python
# make reference to string
s = "Kulik"

# getting slices
print(s[2:4])  # start:end
print(s[:3])   # :end
print(s[4:])   # start:
```

### Output
```
li
Kul
k
```

## String searching
- **find(searchstring)** returns the first index of a character/substring or -1 if it does not exist in the searched string.
- **find(searchstring, index)** returns the first index of the found searchstring starting at the provided index.

```python
# make reference to string
s = "kulik"

# print all indexes of the letter 'k'
i = s.find('k')
while(i != -1):
    print(i, end=', ')
    i = s.find('k', i+1)
print()

# find works with substrings
sub = 'l'
i = s.find(sub)
print(s[i:])
```

### Output
```
0, 4,
lik
```

## String manipulation
- These methods do not change the original string - they return a new one
- **upper()** and **lower()** returns all CAPS or lowercase, respectively
- **replace(this, that)** returns a new string will all occurrences of *this* replaced with *that*

```python
s = "kulik"
print(s)

# get copy of s in CAPS or lowercase
# doesn't change s
print(s.upper())
print(s.lower())

# get copy with replaced chars
print(s.replace('k', 'c'))

# remember: s hasn't changed
print(s)

# reassign to change s
s = s.upper()
print(s)
```

## Output
```
kulik
KULIK
kulik
culic
kulik
KULIK
```

## String split & join
- **split()** will split a string using whitespace and return a list of strings
- **split(separator)** will split a string using a specified separator and return a list of strings
- **joinlist)** will return a list as a string joined with the calling object

```python
# define & print string with spaces
ss = "This is a test"
print( ss )

# split by spaces
ls = ss.split()
print( ls )

# rejoin with commas
ss = ','.join(ls)
print( ss )

# split by commas
ls = ss.split(',')
print( ls )
```

### Output
```
This is a test
['This', 'is', 'a', 'test']
This,is,a,test
['This', 'is', 'a', 'test']
```
