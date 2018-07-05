---
title: "Project 01 - Calculators"
---

## Overview

- Use Python to solve a variety of generalized mathematical problems.
- Your solutions should work for **any** valid input.

## Problems

### 1. Elapsed Time

In the provided template file ```time.py```, write a python program that
will ask for the starting time in 24 four format and duration and output (print)
the end time.

- Input
  - Starting time (24 hour format)
  - time duration in hours

- Output
  - The end time

![](/images/cp1/unit-02/time-demo.gif)

### 2. Tips

In the provided template file ```tips.py```, write a python program that will ask
for the cost of a meal, the tax rate (as decimal), and tip rate (as decimal) and output
(print) the total amount to pay

- Input
    - cost of a meal
    - tax rate (as a decimal, for example 9% is 0.09)
    - tip rate (as a decimal, for example 0.20)

- Output
    - total amount to pay
- Note
    - tax and tip should both be a percent of the base meal cost
    - Hint: there is a built-in function to **round** numbers

![](/images/cp1/unit-02/tips-demo.gif)

### 3. Celsius to Fahrenheit

In the provided template file ```ctof.py```, write a python program that will ask for the
temperature in degrees Celsius and output (print) the degrees in Fahrenheit.

- Formula

    - $$F^{\circ} = C^{\circ} \cdot \frac{9}{5} + 32$$

- Input
  - Degrees Celsius
- Output
  - Degrees Fahrenheit

![](/images/cp1/unit-02/ctof-demo.gif)


### 4. Fahrenheit to Celsius

In the provided template file ```ftoc.py```, write a python program that will ask for the
temperature in degrees Fahrenheit and output (print) the degrees in Celsius.

- Formula
  - $$C^{\circ} = (F^{\circ} - 32) \cdot \frac{5}{9}$$

- Input
    - Degrees Fahrenheit
- Output
  - Degrees Celsius

![](/images/cp1/unit-02/ftoc-demo.gif)

### 5. Interest

In the provided template file ```interest.py```, write a python program that will ask for the
principal, annual interest rate, number of times compounded, and number of years and output
(print) the final amount.

- Formula

    - $$P' = P \Big( 1 + \frac{r}{n} \Big)^{nt}$$

- Input
    - principal amount (```P```)
    - annual nominal interest rate (```r```)
    - number of times the interest is compounded per year (```n```)
    - number of years (```t```)
- Output
    - final amount (```P'```)

![](/images/cp1/unit-02/interest-demo.gif)

### 6. Distance

In the provided template file ```distance.py```, write a python program that will ask for
two points: x1, y1, x2, and y2 and output (print) the distance between the two points

- Formula

    - $$d = \sqrt{(\Delta x)^2 + (\Delta y)^2} = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

- Input
    - first point x (```x1```)
    - first point y (```y1```)
    - second point x (```x2```)
    - second point y (```y2```)
- Output
    - approximate distance

![](/images/cp1/unit-02/distance-demo.gif)

### 7. Change

In the provided template file ```change.py```, write a python program that will ask for a price
and the amount of given currency and will output (print) the numbers of 20s, 10s, 5s, 1s, .25s,
,10s, .05s, and .01s

- Input
    - price
    - amount paid
- Output
    - total change amount
    - amount of each currency denomination (from 20s to pennies) that should be returned

![](/images/cp1/unit-02/change-demo.gif)


### 8. Madlib

- Make a madlib!
- For examples, see [http://www.madglibs.com/]( http://www.madglibs.com/)

<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

<script>
MathJax.Hub.Config({
    jax: ["input/TeX","output/HTML-CSS"],
    displayAlign: "left"
});
</script>
