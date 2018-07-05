---
title: "Lesson 01 - Conditions and Logic"
---


## References

- Tutorialspoint: [Python Decision Making](http://www.tutorialspoint.com/python/python_decision_making.htm)

## Booleans and boolean operations

- **Boolean** is a data type with two possible values: True or False
- The **comparison operators** are used to produce expressions that evaluate to a boolean type
    - a > b
        - True if a is greater than b
    - a >=b
        - True if a is greater than or equal to b
    - a < b
        - True if a is less than b
    - a <= b
        - True if a is less than or equals to b
    - a == b
        - True if a is equal to b
    - a != b
        - True if a is not equal to b
- Boolean operations on **numbers** behave as you would expect
- Boolean operations on **strings** compare lexicographically (by ASCII code)
    - 0 < A < B < a < b
        - True if a precedes b

## Conditional Statements

- **Conditional statements** are used to execute some code only if a certain condition (boolean expression) is met
    - Commonly known as **if-else** statements,but the **else** clause is optional
- if you have more than two conditions, you can **chain** or **nest** conditionals
    - view the [reference](http://www.tutorialspoint.com/python/python_decision_making.htm) for flow charts

### Conditional Examples

```python
x = 5

# if without else
if ( x > 0 ):
    print( "x is positive" )



# if-else
if ( x > 0 ):
    print( "x is positive" )
else:
    print( "x is not positive" )

# chaining is used when there are more than 2 cases
if ( x > 0 ):
    print( "x is positive" )
elif( x==0 ):
    print( "x is zero" )
else:
    print( "x is negative" )

# nesting - the inner conditional is only evaluated if the first is true
if( x > 0 ):
    if ( x%2 == 0):
        print( "x is positive and even" )
    else:
        print( "x is positive and not even" )
else:
    print( "x is neither positive nor even" )
```

## Logic / Boolean operators

- **Logical operators**, also known as **boolean operators**, operate on boolean values
- The main logical operators are **and**, **or**, **not**
    - p and q
        - True if p and q are both True
    - p or q
        - True if either p or q (or both) are True
    - not p
        - True if p is False
- Logical operators can simplify conditionals

### Boolean operator examples

```python
# conjunction (and)
if( x>0 and x%2==0 ):
    print( "x is positive and even" )

# disjunction (or)
if( x>10 or x<-10 ):
    print( "the absolute value of x is greater than 10" )

# negation (not)
if( not (x>10 or x<-10) ):
    print( "the absolute value of x is less than 10" )
```

## DeMorgan's Laws
- DeMorgan's laws can simplify more complex boolean equations
    - "not(A and B)" is the same as "(not A) or (not B)"
    - "not(A or B)" is the same as "(not A) and (not B)"

```python
x = 5

# "not (A or B)"
if( not (x>10 or x<-10) ):
    print( "the absolute value of x is less than 10" )

# "(not A) and (not B)"
if( not(x>10) and not(x<-10) ):
    print( "the absolute value of x is less than 10" )
```
