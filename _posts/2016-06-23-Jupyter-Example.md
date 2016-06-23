---
layout: post
title: "Example with Jupyter Notebook"
date: 2016-06-23
---
The purpose of this notebook is only to experiment with integrating it into my blog. So let's run some simple python statements and see how things come together!


```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
%matplotlib inline
import seaborn as sns
```

I will load the infamous Iris dataset. I can do so from Seaborn:


```python
data = sns.load_dataset('iris')
```


```python
data.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sepal_length</th>
      <th>sepal_width</th>
      <th>petal_length</th>
      <th>petal_width</th>
      <th>species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.9</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
  </tbody>
</table>
</div>



Just so that I have a plot, I will make a pairplot of this dataset - essentially, a scatter plot where the axis are all the pairs of columns. The diagonal shows the distribution of each column in a histogram. The colors correspond to the species of irises in the data.


```python
sns.pairplot(data, hue="species")
```




    <seaborn.axisgrid.PairGrid at 0x9d5c630>




![png](/notebooks/Example_files/Example_6_1.png)

