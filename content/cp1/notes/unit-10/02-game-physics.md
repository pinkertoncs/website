---
title: "Lesson 02 - Game Physics"
---

## Scalar and Vectors

- speed is a **scalar**
  - scalar data only has magnitude
  - for example, 30 mph in forward or reverse is the same speed
- velocity is a **vector**
  - vector data has magnitude and direction
  - the velocity depends on a reference axis
  - the negative and positive directions are arbitrary - they are just that way because
  we said so, it could just as well be t he opposite
  - something traveling to the right at a speed of 30mph, has a velocity of +30mph
  - something traveling to the left at a speed of 30mph, has a velocity of -30mph

![](/images/cp1/unit-10/axis.png)

<br />

## 2D Coordinates

- When we are working in two dimensions, we need two axes.
- Typically, the horizontal is called the x-axis and the vertical is called the y-axis
- In science course, usually up is positive and down is negative
  - in HTML5 Canvas, the opposite is true: __**down is positive and up is negative**__

![](/images/cp1/unit-10/coords.png)

<br />

## Collision Detection and Reflection

- Suppose we want to make a ball bounce around the canvas
  - We will need to detect when the ball reaches the edge of the canvas
  - When the ball reaches the bottom edge, we need to change it's y-velocity so that
  it is going up
- To implement this
  - We will need to store the velocity
  - We can use conditional statements to detect collisions

```javascript
/* rest of code is same as as animation demo */

function update(){

  // canvas.height is the y-position of the BOTTOM of the canvas
  if( pos.y >= canvas.height ){
    vel.y *= -1
  }

  pos.x += vel.x;
  pos.y += vel.y;
}
```

<br />

## Gravity

- Gravity is the force that attracts objects.
- Gravity is a very weak force so it's effects are only noticeable with very large objects,
e.g. the Earth.
- Gravity accelerates objects towards the Earth's surface at:

    - $$\sim32 \mathrm{ft} / \mathrm{s}^2$$
    - In other words, the velocity of an object in free fall increases by 32 ft/s, every
    second (until terminal velocity is reached).
- Your program doesn't have to have the same conditions as earth, so your "gravity" just
needs to be a constant acceleration of one object towards another.
    - To simulate gravity in the +y direction, just increase the y-velocity every tic.



## 2D Velocity and Position

- If an object is moving in a two dimensional plane, we can represent it's velocity in a few ways,
  - a magnitude and a direction (angle)
  - x and y components of velocity called:
      - $$v_x$$
      - $$v_y$$
  - We can go back and forth between these representations using **trigonometry** (yay!)
    - ![](/images/cp1/unit-10/trig.png)
  - JavaScript trig functions use radians instead of degrees
    - To convert use this formula:
      - $$radians = degrees \cdot (\pi / 180 )$$
    - Remember that +y is down, so the **unit circle is inverted
      - ![](/images/cp1/unit-10/unitcirc.png)

```javascript
// magnitude & direction
v = 10
angle = 270

// convert to vx, vy
radians = angle * ( Math.PI / 180 )
vx = v * Math.cos( radians )
vy = v * Math.sin( radians )
```

<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

<script>
MathJax.Hub.Config({
    jax: ["input/TeX","output/HTML-CSS"],
    displayAlign: "left"
});
</script>
