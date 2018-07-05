---
title: "Lesson 01 - Procedures"
---

A **function**/**procedure** is a named set of instructions that can be executed on command

To define a **function**/**procedure**, the programmer needs to write the **header** and **body**

### Header

The header line begins with the keyword **def** and the programmer defined name of the function, followed by parentheses.

The header may or may not take **parameter(s)** in the parentheses, separated by commas.

**Parameters** are a mechanism of giving information *to* the **function**/**procedure**

### Body

The body (which is indented one level), is the set of instructions associated with this function.

The body may or may not have a **return** value. A **return** is a mechanism to receive information back *from* the **function**.

## Calling a Function/Procedure

To **call** a function/procedure, is just to use it's name followed by parentheses (and possible arguments)

## Example

```python
# define the procedure, but don't execute the body yet…
def foo():
    msg = "Hello, world!"
    #return
    #uncomment the return statement to exit early
    print( msg )

# call the procedure 3 times
foo()
foo()
foo()
```

## More input validation / Nested blocks

- If you put a block of code inside of another block, you need to **nest** the blocks using indents
    - You can indent a block by highlighting it and pressing the "Tab" key
    - You can un-indent a block by using Shift-Tab

```python
def getANumber():

    try:
        x = int(input("Enter a number: "))
        # try to read an int
        print("you entered:", x)
    except:
        print("I said enter a number!")
        return
         # use return to exit the function early

    # continue to do stuff with valid input…

getANumber()
```
## Program structure

- A well organized program is easier to write, read, and maintain!
- The template below is a good starting point

```python
"""
Name:
Assignment
"""

def proc1():
    print( "boo!" )


def proc2():
    print( "blah blah blah" )

#--------test procedures in a function called 'main'

def main():
    proc1()
    proc2()

#---------- run main if this file is run
if __name__ == "__main__":
    main()

```

## Using a test input file
- When you are testing, you should read input from a file
- In order to **redirect** the input function so that it reads from a file (e.g. 'input.txt'), insert the code below at the beginning of your program
- Also, make sure you close the file (see modified \_\_main\_\_ below)

```python
#-------------- redirect input
f = open('input.txt')
def input( s='' ):
    line = f.readline()
    # skip comments / blank lines
    if( line[0] in ['#','\n'] ):
        return input(s)
    return line.strip()

#--------------
# DEFINE PROCEDURES HERE
#---------------

def main():
    # CALL PROCEDURES HERE
    pass

if __name__=="__main__":
    try:
        main()
    finally:
        f.close()
```
