---
title: "Lesson 01 - JavaScript"
---


## References

- [JavaScript Tutorial](http://www.w3schools.com/js/)
- [JavaScript Reference](http://www.w3schools.com/jsref/default.asp)

## Getting Started

- JavaScript allows a website to be interactive and dynamic
- JavaScript is included in a ```<script>``` element.
    - Using the ```src``` attribute allows you to load JavaScript from an external file

``` html
<!DOCTYPE html>
<html>
    <head>
        <title>Template Page</title>
    </head>
    <body onload='main()'>
        <h1> JavaScript Template </h1>
        <h2> Hello JavaScript! </h2>
        <p> Go to the JS Console (F12) </p>

        <!-- optional external JS file
        will show error if file doesn't exist  -->
        <script src='myscript.js'></script>

        <script>

            /* multi-line JS comment */
            // single-line JS comment

            function main(){
                console.log( 'Hello, World!' )
            }
        </script>
    </body>
</html>
```

## Basics

- JS expressions and types are similar to Python
- User the **var** keyword to declare a variable
    - In JS, you can **declare** a variable without initializing it
    - an undeclared variable has an **undefined** value
- **Increment** (increasing by 1) the value of an integer
    - ```i = i + 1```
    - ```i += 1```
    - ```i++```
    - ```++i```

### Example
``` javascript
var x;
console.log(x)

x=5
console.log(x++)
console.log(++x)
```

### Output
```
undefined
5
7
```

## Conditions

- Conditions syntax
    - Conditions must be in parentheses
    - Blocks in JS are enclosed in **curly braces {}**
    - curly braces are only required if the block has more than 1 statement
    - Unlike Python code, indentation does not matter (except for style)
    - JS has no ```elif```, you need to use the full ```elseif``` for chaining conditions
- Boolean Operations

| Python | JavaScript |
| --- | --- |
| ```and``` | ```&&``` |
| ```or``` |  &#124;&#124; |
| ```not``` | ```!``` |

### Example

``` javascript
var x = 5;

// chained conditions
// the 'else if' and 'else' clauses are optional
if( x > 0 ){
  console.log( 'x is positive' )
} else if (x == 0) {
  console.log( 'x is zero' )
} else {
  console.log( 'x is negative' )
}

// nested conditions
if( x > 0 ){
  if( x%2 == 0 ){
    console.log('x is positive and even' )
  }
}

// boolean AND
if( x > 0 && x%2==0 ){
    console.log('x is positive and even' )
}

```

## Strings

- see [JS String Reference](http://www.w3schools.com/jsref/jsref_obj_string.asp)

| JS operators / attributes / methods | Description |
| --- | --- |
| ```+``` | string concatenation |
| ```length``` | get the number of characters |
| ```indexOf(sub, i)``` | find substring (*sub*) starting at index *i* |
| ```slice(start, end)``` | get a substring start at *start* and stopping at *end-1* |
| ```toLowerCase()``` | returns string as all lower |
| ```toUpperCase()``` | returns  string as all UPPER |

### Example

``` javascript
var s = "Mr. Kulik"

console.log( s.length )
console.log( s + ' ' + s )
console.log( s.toUpperCase() )

console.log( s.indexOf('uli') )
console.log( s.slice(0,4)  )
console.log( s.slice(4)  )

console.log( s.split(' ') )
```

### Output

```
9
Mr. Kulik Mr. Kulik
MR. KULIK

5
Mr.
Kulik

["Mr.", "Kulik"]
```

## Arrays

- JS Arrays are just like Python's List type
    - Note that you can not use the ```+``` operator to concatenate arrays
    - Splicing is a powerful method the add or remove elements
- Debugging
    - you can log (i.e. print) and array object and inspect it
    - or use ```toString()``` to convert to *neat* representation

| Array operations / methods / attributes | Description               |
| --- | :-------- |
| ```[]``` | index operator |
| ```length``` | length attribute |
| ```indexOf(e, i)``` | return the index of element *e* starting at index *i* |
| ```slice(start, end)``` | return part of the array from *start* to *end-1* |
| ```push(e)``` | add element *e* to the end of the array |
| ```concat(a)``` | add all the elements of array *a* to the end |
| ```shift()``` | remove and return first element |
| ```pop()``` | remove and return last element |
| ```splice(i, n, item1 ... item2)``` | start at *i*, remove *n* things, add remaining |

### Example

``` javascript
var a = ['bread', 'eggs', 'cheese','milk']

console.log( a.toString() )
console.log( a.length )
console.log( a.indexOf('cheese') )
console.log( a[2] )
console.log( a.slice(1,3).toString())

a.push( 'broccoli' )
var a2 = ['bananas', 'apples']
a = a.concat( a2 )
console.log(a.toString())

console.log( a.shift() )
console.log( a.pop() )
console.log( a.toString() )

// remove 3 items at index 1
// and add 'cookies'
a.splice( 1, 3, 'cookies' )
console.log(a)
```

### Output

```
bread,eggs,cheese,milk
4
2
cheese
eggs,cheese
bread,eggs,cheese,milk,broccoli,bananas,apples
bread
apples
eggs,cheese,milk,broccoli,bananas
eggs,cookies,bananas
```

## Loops & Iteration

- JS while loops similar to Python while loops
- JS uses *C-style* for loops
- Syntax: **for(initialization; condition; post-operation)**
    - **initialization** is performed once at the beginning of the loop
    - **condition** determines when the loop stops
    - **post-operation** is performed after each run of the loop
- Example: **for(var i = 0; i < 10; i++)**

| Code | Description |
| --- | --- |
| ```var i = 0``` | initialize a counter variable, *i*, to 0 |
| ```i < 10```  | loop as long as *i* is less than 10 |
| ```i++``` | after each loop, increment *i* by 1 |

### Example 1

``` javascript
// while loop to count from 0 to 4
var i = 0
while( i < 5){
  console.log( i )
  i += 1
}
```

### Output 1

```
0
1
2
3
4
```

### Example 2

``` javascript
// for loop to count from 0 to 4
for( var j = 0; j < 5; j++){
  console.log( j )
}
```

### Output 2

```
0
1
2
3
4
```

### Example 3

``` javascript
// array iteration
var a = ["bread", "eggs", "milk"]
for( var i=0; i<a.length; i++ ){
  console.log( a[i] )
}
```

### Output 3

```
bread
eggs
cheese
```
### Example 4

``` javascript
// string iteration
var s = "Mr.K"
for( var i=0; i<s.length; i++ ){
  console.log( s[i] )
}

```

### Output 4

```
M
r
.
K
```
### Example 5

``` javascript
// string tokenizing
var s = "How are you?"
var tokens = s.split(' ')
for( var i=0; i<tokens.length; i++){
  console.log(tokens[i])
}
```

### Output 5

```
How
are
you?
```

## Functions

- JS functions are similar to Python functions
    - Parameters and return values are optional
    - A function with no parameters still needs ```()```
    - A function with no return statement will return ```undefined```
    - Review parameters and return values if needed
- Two different ways to define functions

``` javascript
// method 1
function foo( a, b ){
  return a + b
}

// method 2
var goo = function(a, b){
  return a + b
}

// function calls
console.log( foo( 1, 2 ) )
console.log( goo( 'me',  'you' ) )
```

## Objects

- JS Objects are similar to Python Objects
- Variables in objects are called **object properties**

### Example

``` javascript
// define object properties
// on initialization
var point = {
  x: 1,
  y: 2
}

console.log( point.x )
console.log( point.y )

// define object properties
// after initialization
var obj = { }
obj.prop1 = 'a'
obj.prop2 = 'b'

console.log( obj.prop1 )
console.log( obj.prop2 )

// turn object into string
console.log( JSON.stringify( obj ) )
```

### Output

```
1
2
a
b
{"prop1":"a","prop2":"b"}
```
