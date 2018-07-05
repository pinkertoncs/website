---
title: "Lesson 04 - Event Handling"
---


## References

- [W3Schools HTML DOM Events Tutorial](http://www.w3schools.com/js/js_htmldom_events.asp)
- [W3Schools HTML DOM Event Object Reference](http://www.w3schools.com/jsref/dom_obj_event.asp)

## Overview

- You've already used event handling!
- When you specify a function for a button's **onclick** attribute,
    - the **event** is **onclick**
    - when the button is clicked, the event if **fired** (a.k.a. **raised**, **triggered**)
    - the **event handler** is the function you specify
- Review your button click handling code from previous notes/worksheets/etc.

## Assigning Event Handlers

- Three ways to do this
    - Set attribute in HTML
    - Set attribute in JS
    - Use **addEventListener** function

#### HTML

``` html
<button onclick='foo()'> Method 1  </button>
<button id=b2> Method 2 </button>
<button id=b3> Method 3 </button>
```

#### JS

``` javascript
function foo(){ console.log('foo') }
function goo(){ console.log('goo') }
function hoo(){ console.log('hoo') }

// method 2
b2.onclick = goo;

// method 3
b3.addEventListener( 'click', hoo );
```

## Anonymous functions
- You can implement functions directly as event handlers, rather than defining them separately
- **Anonymous functions** are not named, nut assigned directly as event handlers

``` javascript
// method 2 with anonymous function
b2.onclick = function(){
  console.log( 'goo' )
}

// method 3 with anonymous function
b3.addEventListener( 'click', function(){
  console.log( 'hoo' )
})  // don't forget to close the parentheses here!
```

## Form input change events

### **oninput and onchange**

- These event handlers will fire when input changes
    - **oninput**: continuously updates as input
    - **onchange** updates when focus moves away from the input
- Note: the keyword **this(( gives you a reference to the element that is being used

#### HTML

``` html
<input oninput='updateText(this.value)'/>
<span id='result1'></span> <br>

<input oninput='updateRange(this.value)' type='range' min=0 max=5/>
<span id='result2'></span>
```

#### JS

``` javascript
function updateText(val){
    result1.innerHTML = val
}

function updateRange(val){
    result2.innerHTML = val
}
```

#### Result

![](/images/cp1/unit-09/event1.png)

## File input - loading a picture
- To select a profile picture, use a ```<input type='file'>``` element
- Attach an event listener to this input, so you know when the file has been selected
- Use a ```FileReader``` object to load the file and display it

#### HTML

``` html
<input type='file' id='fopen'>
<img id='pic'>
```

#### JS

``` javascript
fopen.addEventListener( 'change', function(e){
  var reader = new FileReader()
  reader.onload = function( evt ){
    pic.src = evt.target.result;
  }
  reader.readAsDataURL( fopen.files[0] )
})
```

## Input Devices

### Mouse Events

- [Demo](https://repl.it/HC2J/1)
- Useful mouse events
    - ```onclick```
    - ```onmouseover``` / ```onmouseout```
    - ```onmousedown``` / ```onmouseup```
    - ```onmousemove```
- **click** function with **event** parameter
    - **event.target** is a reference to the element that received a click event
    - **event.x**/**y** are coordinates relative to the upper-left corner of the page
    - **event.offsetX**/**offsetY** are relative to the containing element

``` javascript
document.body.onclick=function(event){

  console.log( event )
  console.log( event.target )  // this is the element that was clicked
  console.log( event.x, event.y )

}
```

### Keyboard events

- [Demo](https://repl.it/HC2O/1)
- From now on, we will specify most event handlers using DOM
- In the ```initialize()``` function, get a handle to the document body ( or whatever element you want to handle keyboard events), and set it's **onkeyup** attribute
- Why **onkeyup**?
    - **onkeydown** repeats for as long as the key is depressed
    - **onkeyup** only fires once per key press
- Notice that **keyup** function takes a parameter **event**
    - **event** is a JS keyword - the parameter is an event object
    - Inspect the event object in the JS debugger
    - Check out the values of **event.keyCode**

``` javascript
document.body.onkeyup=function(event){
    console.log( event.keyCode )
}
```
