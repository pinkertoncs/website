---
title: "Lesson 08 -  Type Casting"
---

Python has built-in functions that enable the programmer to convert or **type cast** data from one format to another.

Type conversion function:
- **int(param)**
    - attempt to convert param to an int
- **float(param)**
    - attempt to convert param to float
- **str(param)**
    - attempt to convert param to string

## Important

The **input** function returns all data as strings, so for example if you ask the user to enter a number for age, it will need to be **type cast** into a **int** before the programmer can use it as a number

## Example

```python
x = input('first number')
y = input('second number')

# the next statement will produce an error - you can't divide strings!

print(x / y)

# below is one solution

x = float(x)
y = float(y)

print(x / y)
```

## Error Handling

To handle the error in case the user enters a string when expecting a number, you can use a **try-catch statement**

- if an error occurs in the 'try' block, control will immediately go the the 'except' block
- if no errors occur in the 'try' block, the 'except' block will not execute

## Example

```python
x = input('Enter a number: ')

try:
    x = int(x)
    print("you entered:", x)
except:
    print("I said enter a number!")
```

## Errors

- **Syntax errors** are the result of spelling errors or malformed expressions
    - CaPitaliZation mismatches
    - not closing quotes or parentheses
- **Runtime errors** are the result of illegal operations
    - dividing by zero
    - trying to divide strings
- **Semantic errors** are errors that the computer will not catch
    - "programmer logic errors"
    - misunderstanding of operator precedence
