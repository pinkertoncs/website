---
title: "Worksheet 01 - Dynamic HTML"
---

## Direction

- create a web page to demonstrate dynamic page components
- write your answers in the provided template (dom.html)

## HTML DOM & Forms

- Answer in the HTML Section

![](https://www.w3schools.com/js/pic_htmltree.gif)

1. What is the DOM?
2. Answer using the diagram above (include the diagram on your web page)
    - What is the parent node of the ```<body>``` element?
    - What are the child nodes of the ```<body>``` element?
    - What is the sibling of the ```<body>``` element?
3. Create a div / form with the following elements
    - text input
    - password input
    - textarea
    - select menu (3 or more options)
    - radio button (3 or more options)
    - checkboxes (3 or more options)
    - a submit button

## JavaScript DOM methods

- Answer in the script section

1. Demonstrate the following DOM access methods
    - ```document.getElementById```
    - ```document.getElementsByTagName```
    - ```document.getElementsByClassName```
    - ```document.getElementsByName```
2. Use the DOM to get
    - All the child nodes of the div/form from question 3 above
    - The parent node of one input
    - The previous sibling on one input
    - The next sibling on one input
3. Use ON methods and the div/form above to log or display the following when you click on the button
    - The text in a text input or text area
    - The selected options from the select menu
    - The checked radio button in a group
    - All checked checkboxes in a group
4. Use DOM to
    - get / set the innerHTML of an element
    - get / set the attributes of an element
    - get / set CSS properties
5. Use the DOM to create and element and append it to the ```<body>``` or a container ```<div>```

## Event Handling

- Answer in the script section

1. Use **onclick** with the event object to get a reference to the clicked element. Modify an attribute of that element
2. Create another text input and button (or use one above). Assign a keyboard event handler so when you hit enter in the text box, the button is effectively clicked
3. Use event handling to mirror the text input in a div as it's being typed
