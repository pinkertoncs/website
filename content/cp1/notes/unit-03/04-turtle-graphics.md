---
title: "Lesson 04 Turtle Graphics (Modules)"
---

# Modules

- A **module** is a collection of code
    - every file you create is a module of your own
    - you can **import** modules to use in your code

```python
import random

# random float 0 <= x < 1
print(random.random())

# random integer 0 <= x < 100
print(random.randrange(0, 100))
```

# Turtle Graphics

## References

- [Turtle](https://docs.python.org/3.4/library/turtle.html)

## Turtle

- **turtle** is a module that allows you to create drawings with Python
- A **class** is a template for creating objects.
    - In the example below, **Screen** and **Turtle** (note the capital 'T') are classes.
- An **object** is a specific instance of a class.
    - In the example below, joe and moe are objects of type 'Turtle'
- The **dot operator (.)** allows you to access attribute and methods of objects
    - **attributes** are properties of an object. For example, turtles have a color, etc.
    - **methods** are actions that an object can perform.
    For example, you can use a turtle to draw!

```python
import turtle

def do_turtle_stuff():

    # create turtles
    joe = turtle.Turtle()
    moe = turtle.Turtle()

    # draw stuff!
    joe.forward(100)


def main():
    try:
        # create a screen
        s = turtle.Screen()
        do_turtle_stuff()
    finally:
        s.mainloop()


main()
```

## Turtle drawing

- For a complete list, check the [Python turtle doc](https://docs.python.org/3.4/library/turtle.html)
- Getting attributes
    - p = t.pos()
        - set variable 'p' to current turtle position
- Setting attributes (assuming instance of turtle, t)
    - t.penup()
        - sets the turtle to movement mode (no drawing)
    - t.pendown()
        - sets the turtle to drawing mode
    - t.width()
        - sets the width of the drawing stroke
    - t.color()
        - sets the pen color
- Movement methods
    - t.goto(x, y)
        - move to a specific location
    - t.forward(dist)
        - move forward
    - t.backward(dist)
        - move backward
    - t.seth(heading)
        - point to specified direction (0:E, 90:N, etc)
    - t.right(angle)
        - turn to the right
    - t.left(angle)
        - turn to the left
    - t.circle(radius, extent)
        - move along an arc

```python
import turtle

def do_turtle_stuff():

    # create turtles
    joe = turtle.Turtle()
    moe = turtle.Turtle()

    # set pen color
    joe.color('blue')
    joe.width(3)

    # draw a nose
    joe.forward(100)
    joe.left(135)
    joe.forward(100)
    joe.right(45)

    # move to another pos w/o drawing
    joe.penup()
    joe.forward(100)
    joe.pendown()

    # draw eyes with radius 75
    joe.circle(75)
    joe.penup()
    joe.right(90)
    joe.forward(50)
    joe.pendown()
    joe.right(90)
    joe.circle(75)

    # move to position for mouth...
    joe.penup()
    joe.forward(200)
    joe.right(90)
    joe.forward(200)
    joe.left(90)
    joe.pendown()

    # draw a semicircle
    joe.circle(200,180)


def main():
    try:
        # create a screen
        wn = turtle.Screen()
        do_turtle_stuff()
    finally:
        wn.mainloop()


main()
```

Result of sample code

![](/images/cp1/unit-03/face.png)
