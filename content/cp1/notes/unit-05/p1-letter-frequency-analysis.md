---
title: "Project 01 - Letter Frequency Analysis"
---

## Directions

- use the provided template code as your starting point
- implement the functions where you see **pass**

## Tips

### **read_file(filename)**

- opens a file and passes each line to the **parse_sentence** function


### **parse_sentence(line)**

- passes each word of *line* to the **analyze_word** function.

### **analyze_word(word)**

- reads each character of 'word', if it is a letter update the *letter_freq* dictionary accordingly
- Should case matter?
- How do you know if a character is a letter?

### **make_graph()**

- what type of graph do you think best helps visualize the letter frequency of a piece of text (pie, line, bar, other)?
- Using your gathered letter frequency metrics, plot your data

### **preprocess_data()**

- this helper function converts the the dictionary of letters and frequency to a tuple containing the letters (keys) and frequencies (values)

- This may help you in preparing your data for plotting.

## Sample Output

 This sample shows the letter frequency of the provided *test-input.txt* to help with debugging purposes.

 ```
 {'D': 28, 'C': 45, 'G': 19, 'I': 89, 'F': 11,
  'U': 100, 'H': 3, 'L': 55, 'N': 61, 'T': 68,
  'X': 2, 'Q': 16, 'P': 28, 'M': 37, 'E': 103,
  'A': 85, 'V': 16, 'B': 10, 'O': 40, 'S': 82,
  'J': 2, 'R': 54}
```
