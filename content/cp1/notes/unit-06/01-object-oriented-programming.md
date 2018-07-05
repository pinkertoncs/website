---
title: "Lesson 01 - OOP"
---

## References

- Tutorialspoint: [Python object-oriented](http://www.tutorialspoint.com/python/python_classes_objects.htm)

## Review: classes & objects

- A **class** is a template for creating objects.
    - **attributes** are variables local to the class
    - **methods** are functions - they are things the class can do.
- An **object** is a specific instance of a class
- For example, Turtle is a class
    - attributes of turtle include: color, width, position, heading
    - methods of turtle include: forward, left, penup, pendown
- Joe and Moe are objects (instances of Turtle), and each have their own attribute values

```python
# create objects
joe = Turtle()
moe = Turtle()

# pencolor METHOD sets the color ATTRIBUTE
joe.pencolor( 'blue' )
moe.pencolor('green')

# these METHODS change the position ATTRIBUTE of joe
joe.goto(0,0)
joe.forward(100)
```

## Defining classes

```python
class Person:               # empty class definition
    pass

def main():
    joe = Person()          # define a Person object
    joe.name = "Joe"        # give joe a name attribute
    print( joe.name )       # access joe's name
```

## Special methods

- the keyword **self** is the first parameter for all methods
    - self is used to refer to the object that will call the method
- the **\_\_init\_\_** method is the **object constructor**
    - the constructor is automatically called when you create a new object
    - the parameter *n* is used to assign the name of a new Person
    - the default value of "Anonymous" is applied when no name is given
- the **\_\_str\_\_** method is called automatically when you print and object
    - This method should always return a string

```python
class Person:
    # constructor
    def __init__(self, n="Anonymous" ):
        self.name = n

    # string casting method
    def __str__(self):
        return self.name

def main():
    # create some Person objects
    p1 = Person()
    p2 = Person("Joe")

    # print some Person objects
    print( p1 )
    print( p2 )
```

### Output
```
Anonymous
Joe
```

## Regular methods

- Regular methods are called using the **dot operator**

```python
class Person:
    # constructor
    def __init__(self, n="Anonymous" ):
        self.name = n

    # string casting method
    def __str__(self):
        return self.name

    def sayHi( self ):
        print( "Hi, my name is", self.name )

def main():
    joe = Person("Joe")     # define a Person object
    joe.sayHi()             # call say_hello method

main()
```

### Output
```
Hi, my name is Joe
```

## Object composition
- Object composition is when one object contains others
- In this example, the Person object contains a list of hobbies
    - Hobbies are just strings here, but an object can contain instances of other objects!

```python
class Person:
    # constructor
    def __init__(self, n="Anonymous" ):
        self.name = n
        self.hobbies = []

    # string casting method
    def __str__(self):
        return self.name

    def say_hello( self ):
        print( "Hi, my name is", self.name )

        if self.hobbies:
            print( "I like", end=' ' )
            for hobby in self.hobbies:
                print( hobby, end=', ')
            print()

    def add_hobby( self, h ):
        self.hobbies.append( h )


def main():
    joe = Person("Joe")
    joe.add_hobby("skiing")
    joe.add_hobby("trains")
    joe.add_hobby("turtles")
    joe.say_hello()
    print('---')
    sam = Person('Sam')
    sam.say_hello()

main()
```

### Output
```
Hi, my name is Joe
I like skiing, trains, turtles,
---
Hi, my name is Sam
```
