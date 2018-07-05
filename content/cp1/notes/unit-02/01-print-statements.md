---
title: "Lesson 01 - Print Statements"
---

Python has a function (more on those later) **print** that produces output in the interpreter window.

Think of **print** as a way to provide feedback to the user of your program

[Official documentation](https://docs.python.org/3/library/functions.html#print)

We will primarily use one of the following three "flavors"

* **print**
    - "displays" a line break. AKA a newline
* **print(data)**
    - "displays" whatever value (literal or variable) data is
* **print(data1, data2, ...)**
    - prints multiple values on a single line

## Examples

```python
# print a new line
print()
```

```python
#print the number 1
print(1)
```

```python
#print the text 'Hello World'
print('Hello World' )
# or
print("Hello World")
```

```python
#print multiple values per line
print(1, 'Hi', 3.14, 'Class!')
```

# Print Special Characters

The **escape character** (backslash '\\') is used to designate special characters in strings:

Frequently used special characters
- **\\n** newline
- **\\t** tab
- **\\\\** backslash

You can have single/double quotes in strings by nesting them, or by using the escape character.

- wrapping
    - 'This is a "quote" yo'
- escape character
    - 'This is a \'quote\' yo'
