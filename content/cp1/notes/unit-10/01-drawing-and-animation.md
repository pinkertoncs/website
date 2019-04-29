---
title: "Lesson 01 - Drawing and Animation"
---

## References

- Canvas
  - [W3Schools Canvas Tutorial](http://www.w3schools.com/html/html5_canvas.asp)
  - [W3Schools Canvas Reference](http://www.w3schools.com/tags/ref_canvas.asp)
  - [HTML5 Canvas Tutorials](http://www.html5canvastutorials.com/)
- Timing
  - [JS Timing Tutorial](http://www.w3schools.com/js/js_timing.asp)


## Canvas

- See the tutorials for information on the ```<canvas>``` element and context object
- Notes:
  - Use the HTML width and height attributes to set the dimensions of a canvas. Do not use
  CSS, it will just stretch and/or compress the canvas and distort the true dimensions

### HTML
```html
<body onload="initialize()">
    <h1> Canvas! </h1>
    <canvas id="game" width="400" height="250"></canvas>
    <script src="script.js"></script>
</body>
```

### JS
```javascript
var initialize = function(){

    // get the canvas and context
    var c = document.getElementById("game")
    var ctx = c.getContext("2d")

    // ctx properties
    ctx.lineWidth=5
    ctx.strokeStyle='red'
    ctx.fillStyle='blue'

    // line
    ctx.moveTo(50,100);
    ctx.lineTo(100,200);
    ctx.stroke();

    // rectangle - simple
    ctx.fillRect(10,10,150,75)

    // rectangle w/ border
    ctx.rect(200,10,150,75);
    ctx.stroke()
    ctx.fill()

    // arcs and circles
    ctx.beginPath();
    ctx.arc(175,150,40,0,2*Math.PI);
    ctx.stroke();

    // closed path
    ctx.beginPath();
    ctx.moveTo(250,125);
    ctx.lineTo(300,175);
    ctx.lineTo(350,125);
    ctx.closePath();
    ctx.stroke();
    ctx.fill()

    // text
    ctx.font = "30px Arial";
    ctx.fillText("Hello World",10,250);
    ctx.lineWidth=1;
    ctx.strokeText("Hello World",200,250);
}
```

### Result

![](/images/cp1/unit-10/canvas.png)

<br />

## Loading and Drawing Images

- In the following example, we are assigning ```imageObj.onload``` to a function
- The function is called a **callback function** (or just a 'callback')
- The code in the callback will be executed **AFTER** the image is loaded

```javascript
var canvas = document.getElementById('myCanvas');
var context = canvas.getContext('2d');
var imageObj = new Image();

imageObj.onload = function() {
  context.drawImage(imageObj, 69, 50);
};
imageObj.src = 'darth-vader.jpg';
```

<br />
## Timing

- the ```setInterval``` function allows is to repeat a function every given interval value
- Example: ```setInterval( function() { /* YOUR CODE HERE */ }, INTERVAL)```
- Notice that a function is declared, but not named, inside setInterval. This is called an
**anonymous function~~
- Calling your function inside of an anonymous function is called **function wrapping**

```javascript
var stopwatch = setInterval( 'logTime()', 1000 )

var time = 0
function logTime(){
  console.log( time )
  time += 1
}
```

<br />
## Animation

- the draw loop is, clear -> update -> draw
- Global variables, RADIUS, and FPS are actually **constants** - they do not change unless we
change them in the code
- xpos and ypos are used to store the position of the object

```javascript
var canvas = document.getElementById('myCanvas');
var context = canvas.getContext('2d');

var FPS=60;

var ball = {
    x:0,
    y:0,
    vx:1,
    vy:1,
    r:10
}

// detect collisions
function detectCol(){

    // YOUR CODE HERE
}

function update(){
  ball.x += ball.vx;
  ball.y += ball.vy;
}

function draw(){
  context.beginPath()
  context.arc(ball.x, ball.y, ball.r, 0, 2 * Math.PI);
  context.fill()
  context.stroke()
}

function drawLoop(){
  context.clearRect(0,0,canvas.width, canvas.height);
  detectCol()
  update()
  draw();
}

// start the animation
setInterval(drawLoop , 1000/FPS )
```
