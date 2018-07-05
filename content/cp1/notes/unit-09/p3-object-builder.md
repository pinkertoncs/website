---
title: "Project 03 - Object Builder"
---

## Builder function

- Create an HTML form that allows you to choose options for a vehicle (or something of your choosing)
    - (see example below)
- The form should have
    - text input(s)
    - select menu
    - radio buttons
    - checkboxes
    - button
- In your JS function 'build' should
    - read the data from the form
    - construct a JavaScript object (obj) that represents the car (or other object)
    - Log the object to the console for debugging
    - call **view(obj)**

## Viewer function

- In the **view** function
    - create a new ```<tr>``` using DOM method(s)
    - use the properties of the parameter obj passe from the build function to set the innerHTML of the new row you created in step 1
    - append the new row to the view table

## Screenshot - on page load

![](/images/cp1/unit-09/obload.png)

## Screenshot - after building a few cars

![](/images/cp1/unit-09/cars.png)
