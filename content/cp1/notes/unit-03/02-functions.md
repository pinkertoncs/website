---
title: "Lesson 02 - Functions"
---

## Reference

- [Python Functions](http://www.tutorialspoint.com/python/python_functions.htm)

## Overview

- You can think of functions as different parts of your program.
- Just like in math, a function can take one or more inputs and produce output.
    - Function **parameters** are the inputs to the function
    - Function **return values** are the output from the function
    - ![](/images/cp1/unit-03/in-out.png)

## Function scope and local variables
 - Each function has its own set of variables. This is called the function's **scope**
 - Variables defined in functions are **local variables** - they cannot be accessed outside of the function. The print statement below will result in an error
    - *NameError: global name 'msg' not defined*

```python
def foo():
    # variable msg is local to foo
    msg = 'hi'


def main():
    # no variable called msg in main
    print(msg)


main()
```
![](/images/cp1/unit-03/scope.png)

## Parameters

- A **parameter** is a local variable that is initialized when a function is called
    - The **parameter list** is the part of the function header that goes in the parentheses.
    - In the example below, the function goo has a single parameter - msg.
    - Functions can have 0, 1, or more parameters.
- see diagram below
    - the value of *note* is copied to the local variable *msg* in goo's namespace

```python
# goo has one parameter, msg
def goo(msg):   # 3. msg gets the passed value ("hi!")
    print(msg)  # 4. value of msg is printed


def main():
    note = 'hi' # 1. assign the value "hi!" to variable note
    goo(note)   # 2. pass the value of note to goo


main()
```
![](/images/cp1/unit-03/params.png)

## Return statements

- A **return statement** allows you to pass information back to the calling function.
    - *GOTCHA: don't use parentheses in a return statement*
- The information passed back is call the **return value**
- You can *'catch the return value* using a variable assignment.

```python
def hoo():
    msg = 'hi!'  # 2. local variable msg gets value "hi!"
    return msg   # 3. value of msg is returned


def main():
    note = msg() # 1. function hoo is invoked
                 # 4. note gets returned value "hi!"
    print(note)


main()
```
![](/images/cp1/unit-03/return.png)

## Functions in Practice

- It's typical for a function to take some data (parameters) and use it to return some other data (return).
- Follow the numbers to trance the code below

```python
def double( x ):        # 3. x gets the passed value, 5
    return 2*x          # 4. y returns 2*x, 10

def main():
    y = 5               # 1. y gets the value 5
    z = double( y )     # 2. value of y (5) is passed to double
                        # 5. z gets assigned the returned value, 10
    print(z)

main()                  # 0. main is called first
```
