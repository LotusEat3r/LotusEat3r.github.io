---
layout: post
title: "Basic Plotting in Wolfram Mathematica"
author: Dallin Robison
description: "An introduction to using a few of the plot functions in Mathematica"
---

{% raw %}<img src="{{ site.url }}{{ site.baseurl }}/assets/images/53hyp.jpg" alt="">{% endraw %}
# Introduction

Wolfram Mathematica is a powerful tool for data visualization. This article will go through some of the fundamentals of four plotting functions found in Mathematica: `Plot[]`, `ListPlot[]`, `Plot3D[]`, and `ListPlot3D[]`. Other plotting functions exist, and each of them works with a different kind of input, but we will restrict our focus to these four for the sake of simplicity.

Before diving into these functions, there are a few points we should know. For functions, Mathematica uses UpperCamelCase and the square brackets, and it uses curly braces for lists. The formatting will end up looking like this:

```
Plot[f(x), {x, 0, 10}]
```

# Plotting Using a Dataset

In this section, we will look at how to import a dataset and use `ListPlot` and `ListPlot3D` to create a visualization of the data we imported.

### Importing the Dataset 

If your goal is to try to observe correlations in data, you will want to import relevant data sets. Importing will make using the `ListPlot` and `ListPlot3D` functions much more simple to use.

We will use the `Import` function to import our data. `Import` takes a csv, tsv, or xls file and reads the file into a mathematica table. It has two arguments: the name of the file you are reading from and "Table" which means that you want to read the data in as a table.

```
Import[data.csv, "Table"]
```

Mathematica tables are formed by sets of curly braces. Each set of braces creates a layer of the table, or in other words, nesting braces adds a dimension to your table. 

### Two-Dimensional Datasets

If you want to look at the interaction between two variables, then you can use `ListPlot` to create a two-dimensional scatterplot of that relationship. One of the limitations of Wolfram Mathematica is that the data you provide to `ListPlot` must be a table with only two variables. The `ListPlot` function has one argument: the table of values.

```
ListPlot[data]
```

### Three-Dimensional Datasets

Plotting a three-dimensional scatterplot works very similarly to plotting a two-dimensional scatterplot in Mathematica. Instead of `ListPlot`, we will use `ListPlot3D`. You must provide a table with three variables to the function, and this is its only argument.

```
ListPlot3D[data]
```

One of the useful things about Wolfram Mathematica is that the three-dimensional plot is interactive. You can click and drag to rotate the plot in any direction.



# Plotting a Function

Instead of plotting a dataset, say you want to plot a function. Mathematica has another set of functions, `Plot` and `Plot3D`, that do this. 

### Two-Dimensional Functions

`Plot` is useful for visualizing curves. It takes as input a function and a range, and plots the function over that range. For instance, consider the function $f(x)=x^2$. If we wanted to focus on the center of this parabola, we would want to see values of $x \in (-2,2)$. The code for this would be:

```
Plot[x^2, {x, -2, 2}
```

The first argument is the function, and the second argument is a list providing the variable and the range you want to see of the function on that variable.

### Three-Dimensional Functions

Say instead of a curve you want to create a visualization of a surface or three-dimensional object. `Plot3D` does exactly this. It follows a similar form to `Plot`:

```
Plot3D[x^2 + y^2 = 1, {x, 0, 1}, {y, -1, 1}]
```

The first argument is a function of two variables, and the second and third arguments are each variable and the range you want to see the function applied to.

Mathematica also allows you to rotate the plot resulting from these functions, like with `ListPlot3D`.

# Combining Plots

Say you want to plot two things at once, say a function and a dataset. In order to do this in Mathematica, you can use the `Show` function. This function takes the plots you want to combine and returns one plot with everything on it.

```
Show[plt1, plt2]
```

# Conclusion

Now that you have some exposure to these topics, go and interact with these things yourself. The best teacher is experience, so plot functions and datasets. You may find some interesting connections in your data.
