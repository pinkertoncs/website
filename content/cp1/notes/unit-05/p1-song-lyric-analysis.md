---
title: "Project 01 - Song Lyric Analysis"
---

## Directions

- Use the provided template code as the starting point for your project.
- Add your code to the functions where you see **pass**

## Outcome

- You will be using Python and matplotlib to graph the frequency of words in popular songs.
- Use a search engine to find lyrics, and copying them into text files in your repl.it project.
- You should choose songs that are appropriate for school. If there are questionable lyrics
(curse words, etc), us the radio edits as necessary.

## Requirements

- Analyze and plot the data for three(3) songs.

## Question

- What can you infer from viewing your graphs?
  - What words are the most common?
  - What are the songs about?

## Tips

### **read_file(filename)**

- opens a file and passes each line to the **parse_sentence** function

### **parse_sentence(line)**

- passes each word of *line* to the **analyze_word** function.

### **analyze_word(word)**

- If the word does not exist in the dictionary, add it into the dictionary
- If the word **does** exists in the dictionary, update the word frequency by 1 (i.e. increment by 1)
- Considerations
  - Should case matter? (upper v.s. lower)
    - "Cake" v.s. "cake"

### **make_graph()**

- what type of graph do you think best visualizes the word frequency of your songs? (pie, line, bar, other)?
- Using your gathered word frequency metrics, plot your data

### **preprocess_data()**

- this helper function converts the the dictionary of words and frequency to a tuple containing the letters (keys) and frequencies (values)

- This may help you in preparing your data for plotting.

## Sample Output

- Here is an example of the contents of the dictionary and a pie plot of the song "Let it Be" by
The Beatles &copy;.

### Dictionary Contents

```
{'when': 3, 'i': 2, 'find': 1, 'myself': 1, 'in': 4, 'times': 1, 'of': 11, 'trouble': 1,
'mother': 2, 'mary': 2, 'comes': 2, 'to': 3, 'me': 4, 'speaking': 3, 'words': 7, 'wisdom': 7,
'let': 41, 'it': 41, 'be': 26, 'and': 3, 'my': 1, 'hour': 1, 'darkness': 1, 'she': 1, 'is': 4,
'standing': 1, 'right': 1, 'front': 1, 'be,': 21, 'whisper': 4, 'the': 4, 'broken-hearted': 1,
'people': 1, 'living': 1, 'world': 1, 'agree': 1, 'there': 7, 'will': 6, 'an': 5, 'answer': 5,
'for': 1, 'though': 1, 'they': 2, 'may': 1, 'parted': 1, 'still': 2, 'a': 2, 'chance': 1,
'that': 2, 'see': 1, 'yeah,': 4, 'night': 1, 'cloudy': 1, 'light': 1, 'shines': 1, 'on': 1,
'shine': 1, 'until': 1, 'tomorrow': 1, 'wake': 1, 'up': 1, 'sound': 1, 'music': 1}
```

### Plot

![](/images/cp1/unit-05/p1-chart.png)
