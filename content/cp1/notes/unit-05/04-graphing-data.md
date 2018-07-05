---
title: "Lesson 04 - Graphing Data"
---

## Reference

- Python Tutorials [Matplotlib](https://pythonspot.com/en/matplotlib/)
- [Matplotlib Documentation](https://matplotlib.org/api/pyplot_summary.html)

## Background

Matplotlib is the most popular python library for creating graphs and plots.
It is provided to programmers as a module.

```python
import matplotlib.pyplot as plt
```

## Pie Chart

- A pie chart is a circular graph which is divided into slices to illustrate proportions.

```python
import matplotlib
matplotlib.use('Agg')
import matplotlib.pyplot as plt

# graph labels
labels = ['Chicken', 'Fish', 'Steak', 'Vegetarian']

# data
num_dishes = [34, 11, 47, 3]

# colors for slices
colors = ['yellow', 'blue', 'red', 'green']

# create the pie chart
plt.pie(num_dishes, labels=labels, colors=colors)

# equal x and y increments
plt.axis('equal')

# save the graph
plt.savefig('piechart')

```

![](/images/cp1/unit-05/pie.png)


## Bar Chart

- A bar chart is a graph that show information using rectangular bars with lengths that represent their values

```python
import matplotlib
matplotlib.use('Agg')
import matplotlib.pyplot as plt

# graph labels
labels = ['Chicken', 'Fish', 'Steak', 'Vegetarian']

# data
num_dishes = [34, 11, 47, 3]

# get range of elements to plot
x = range(len(num_dishes))

# plot the data
plt.bar(x, num_dishes, align='center')

# label the xticks with the dish name
plt.xticks(x, labels)

# describe the y axis
plt.ylabel('Number of Dishes')

# save the graph
plt.savefig('barchart')
```

![](/images/cp1/unit-05/bar.png)

## Line Chart

- A line chart is graph that shows information as a grouping on points connected by lines.

```python
import matplotlib
matplotlib.use('Agg')
import matplotlib.pyplot as plt

# create a subplot, (1 row , 1 col) aka. 1 plot
# this enables us to change ticks and labels
fig, ax = plt.subplots(1, 1)

# graph labels
labels = ['Chicken', 'Fish', 'Steak', 'Vegetarian']

# data
num_dishes = [34, 11, 47, 3]

# set the x  range/ tick to length of num_dishes
x = range(len(num_dishes))

# create the pie chart
ax.plot(x, num_dishes)

# set the ticks to number of dishes
ax.set_xticks(x)

# set the labels to the food item
ax.set_xticklabels(labels)

# save the graph
plt.savefig('linechart')
```
![](/images/cp1/unit-05/line.png)
