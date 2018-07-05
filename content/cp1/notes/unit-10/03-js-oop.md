---
title: "Lesson 03 - JavaScript  OOP"
---

## References

- [JavaScript Objects](http://www.w3schools.com/js/js_object_definition.asp)
- [JavaScript Prototypes](http://www.w3schools.com/js/js_object_prototypes.asp)

## Overview

- In **object-oriented programming (OOP)**, objects methods are used to program behavior
or "intelligence" into objects.
    - For example, instead of defining functions that update and draw a ball, we can program
    that functionality directly into the ball object itself.
    - This allows for greater code organization and expressiveness.
    - OO programming is now the de-facto standard for non-trivial programs.
- The demos show two different ways of doing object-oriented programming in JavaScript.
  - Demo 1 uses object literals to create single instances of objects.
  - Demo 2 uses object constructors to create multiple instances of objects.

## Objects Revisited

- Object literals are used to create "singletons."
  - If you only need one instance of an object, this is probably the way to go.
- Notice that we're using literals differently than before.
  - The sections of the object declaration are the object's methods.
  - We're declaring attributes of the object using the **this** keyword.  **this** refers
  to the ball itself, so **this.x** becomes **ball.x** when accessed out-of-context.
- After this declaration, we have created a ball object and just need to **initialize** it.
- Since we want this to be OO, we put as much of the ball's functionality into the ball
object as we can.

```javascript
var ball={
    initialize:function(x,y,r){
        this.x=x; this.y=y
        this.r=r
        this.vx=1; this.vy=1
    },
    update:function(){
        this.x += this.vx
        this.y += this.vy
    },
    draw:function(ctx){
        ctx.beginPath()
        ctx.arc(this.x,this.y,this.r,0,2*Math.PI);
        ctx.stroke();
        ctx.fill()
    }
}

// initialize
ball.initialize( x, y r )
```

## Prototypes

- Prototypes are essentially JavaScript's version of classes.
  - If you wanted to create multiple object instances, use prototypes.
- When you use constructors, you must construct new objects using the new keyword.

```javascript
var Ball = function(x, y, r){
    this.r=r
    this.x=x; this.y=y
    this.vx=1; this.vy=1

    this.update=function(){
        this.x += this.vx
        this.y += this.vy
    }

    this.draw = function(ctx){
        // draw game ball in given context at pos (x,y)
        ctx.beginPath()
        ctx.arc(this.x,this.y,this.r,0,2*Math.PI);
        ctx.stroke();
        ctx.fill()
    }
}

// create new Ball objects
var ball1 = new Ball(x1, y1, r1)
var ball2 = new Ball(x2, y2, r2)
```

### Prototype Property

- You can use the prototype property to add properties / methods to an existing prototype.
