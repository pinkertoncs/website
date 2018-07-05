---
title: "Lesson 01 - HTML Basics"
---


## References

- **Primary**: [W3Schools HTML Tutorial](http://www.w3schools.com/html/) - Instructions with interactive examples
- **Secondary**: [Codecademy HTML & CSS](http://www.codecademy.com/en/tracks/web) - Interactive Tutorials (requires login)
    - great for practicing

## Inspecting HTML

- Use [Chrome DevTools](https://developer.chrome.com/devtools)
- You can inspect HTML for any web page by
    - Right Mouse Click -> **Inspect element**


## HTML template

- Please review the primary reference
- You can use the HTML template below to start a new document

```html

<!DOCTYPE html>
<html>
    <head>
        <title>Template Page</title>
    </head>
    <body>
        <!-- HTML Comment -->
        <h1> HTML Template </h1>
        <p> Hello, World! </p>
    </body>
</html>


```

## Basic Elements

- HTML elements are the components of your web page
- HTML elements (usually) have and ```<opening>``` tag and a ```</closing>``` tag
- Non-display elements
    - ```<html> ... </html>```
    - ```<head> ... </head>```
    - ```<body> ... </body>```
- Elements are nested - you can and will put elements inside of other elements
- Display elements
    - ```<h1> headings </h1>```
    - ```<p> paragraphs </p>```
- Some elements do not have a closing tag - put a slash at the end of tag in these cases, e.g.
    - Page break  ```<br/>```
    - Horizontal rule (line): ```<hr/>```

## Links and images

- **Attributes** are like variables that specify something about the element
- Universal attributes (all elements have these)
    - **id** - used to identify a single element
    - **class** - used to identify a group of related elements (more on that later)

- ```<a> Links </a>```
    - **href** hypertext reference. full URL, including http://
    - **target** set to ```_blank```, the link will open in a new tab

    - You can use ```<a>``` to link to
        - a section within the page
        - another ```.html``` file
        - an external web page

    ```html

    <!-- use a hash symbol # to link to a section on this page by id   -->
    <a href='#header1'> Header 1 </a>

    <!-- use a filename or relative filepath to link to another local page -->
    <a href='page2.html'> Page 2 </a>

    <!-- use a full URL to link to an external page -->
    <a href='http://pinkertoncs.github.io'> Pinkerton Academy Computer Science </a>

    <h1 id='header1'> This is Header 1 </h1>

    ```

- image tag ```<img>```
    - **src** filename or relative path; or Full URL of an online image
    - **alt** sets alternative text to be displayed if image can't be loaded
    - **height / width** dimensions in pixels of %. if you set up just one the other will scale automatically

    ```html
    <img src='example.jpg' alt='example image' width='250'/>

    <!-- an image can be nested in a link -->
    <a href='https://goo.gl/aBL6vS'> <img src='https://goo.gl/aBL6vS'/> </a>
    ```

## Structural elements

- tables
    - ```<tr>``` is table row
    - ```<th>``` is table header
    - ```<td>``` is table data (cell)
    - you can use **colspan** or **rowspan** attributes to span multiple columns / rows
- lists
    - ```<ol>``` is ordered list (numbers / letters )
    - ```<ul>``` is unordered list (bullet points)
    - you can use **type** or **list-style-type** attributes to change the marker. (see W3Schools)

    ```html

    <table>
         <tr> <th colspan=2> This th spans 2 columns </th> </tr>
        <tr> <th> header col 1 </th> <th> header col 2 </th> </tr>
        <tr> <td> table data 1 </td> <td> table data 2 </td> </tr>
    <!-- etc… -->
    </table>

    <!-- ol is ordered (numbered) list, use ul for unordered (bullets) -->
    <ol>
        <li> list item 1 </li>
        <li> list item 1 </li>
        <li> list item 1 </li>
    </ol>

    ```

- divs and spans
    - ```<div>``` is a **block-level element** - it takes up the width of the page and the height of the content
    - ```<span>``` is an inline element - it takes up only as much width as the content
    - divs and spans are used for creating layouts (more on this later)

    ```html

    <div> Div 1 </div>
    <div> Div 2 </div>

    <span> Span 1 </span>
    <span> Span 2 </span>
    ```

# Entities

- Some special character can be inserted using HTML entities
- For more into visit:
    - [W3Schools HTML Entities](http://www.w3schools.com/html/html_entities.asp)
- Common used entities
    - ```&nbsp;``` inserts a space
    - ```&lt;``` < symbol
    - ```&gt;``` > symbol
