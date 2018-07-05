---
title: "Project 01 - Word Games"
---

## Objectives

- Use the DOM to access the value of input fields
- Use the DOM to modify the innerHTML of a div
- Use string methods
- Use array methods

## Madlib

- To get started, add these elements to your page
    - text input
    - button
    - paragraph
- Implement the following behavior
    - When you click the button, the text in the input is echoed in the paragraph
- Create more inputs with labels and a single submit button
- When the button is clicked, call a function that generates a story using the information entered and displays it in the paragraph

![](/images/cp1/unit-09/madlib.png)

## Piglatin

- Create a div with a text input, a button, and a paragraph
- When the button is clicked, the text in the input is translated to Pig Latin
- Rules of Pig Latin
    - Words beginning with vowels (a, e, i, o, u) should have **way** appended to them
    - Words beginning with consonants should have the consonant moved to the end and have
    **ay** appended
    - All letters should be lower case

### Example

```
"Hi how are you doing" -> "ihay, owhay, areway ouyay oingday"
```

### Extensions (optional)

- Make the translator work with punctuation
- Make the translator work with words that have multiple letters that make a single sound at the beginning. e.g. "chocolate" -> "ocolatechay"
