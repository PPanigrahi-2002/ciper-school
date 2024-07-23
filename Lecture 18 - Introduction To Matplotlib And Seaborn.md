Introduction to Matplotlib and Seaborn
Definition:
• Matplotlib: Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in ns in Python. It provides an object-oriented API for embedding plots into applications 
using general-purpose Gül toolkits. 
• Seaborn: Seaborn is a Python data visualization library based on Matplotlib. It provides a high-level interface for drawing attractive andinformative statistical graphics.

Use Case in Real Life:
• Data Exploration: Create various plots to visualize data distributions and relationships between variables during the exploratory data analysis (EDA) phase
• Statistical Analysis: Use visualizations to understand statistical properties of datasets, such as distribution plots, histograms, and pair plots to identify correlations and patterns. 
• Business Reporting: Generate business reports with visualizations that provide insights into sales performance, customer behavior, and market trends.

CREATING A SIMPLE LINE PLOT WITH MATPLOTLIB
````````````````````````````````````````````
import matplotlib.pyplot as plt
# Data
x = [1,2,3,4,5]
y = [2,3,4,7,11]
# creating a line plot
plt.plot(x, y)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Simple Line Plot')
plt.show()

STYLING THE PLOT

# Data
x = [1,2,3,4,5]
y = [2,3,4,7,11]
# creating a line plot
plt.plot(x, y, linestyle='dotted/dashed', color = 'r', linewidth/lw = "3", markers = "o", 
          mac/mfc = "r", ms = "20")
# plt.plot(x, y, ls=':/--')      # Solid line(-), Dashdot(-.), None(" ")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Simple Line Plot')
plt.show()

CREATING A SIMPLE SCATTER PLOT WITH MATPLOTLIB
```````````````````````````````````````````````
# Data
x = [1,2,3,4,5]
y = [2,3,4,7,11]
# creating a scatter plot
plt.scatter(x, y, color = "r")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Simple Scatter Plot')
plt.show()

CREATING A SIMPLE BAR PLOT WITH MATPLOTLIB
```````````````````````````````````````````````
# Data
products = ["Pc", "TV", "REF", "Micro"]
sales = [2,3,4,7]
# creating a scatter plot
plt.bar/barh(products, sales, color = "r", width/height = 0.1)
plt.xlabel('Products')
plt.ylabel('sales (in 1000s)')
plt.title('Simple Bar Plot')
plt.show()

CREATING A SIMPLE HISTOGRAM WITH MATPLOTLIB
````````````````````````````````````````````
# Data
data = [1,2,2,3,3,3,4,4,4,4]
# creating a line plot
plt.hist(data, bins = 4)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Simple Histogram')
plt.show()

CREATING SUBPLOTS WITH MATPLOTLIB
`````````````````````````````````
# Data
x = [1,2,3,4,5]
y1 = [2,3,5,7,11]
y2 = [1,4,6,8,10]
# Creating subplots
fig, axs = plt.subplots(2)
axs[0].plot(x,y1)
axs[0].set_title('First Plot')
axs[1].pleot(x,y2, 'tab:orange')
axs[1].set_title('Second Plot')
# Displaying the plot
plt.tight_layout()
plt.show()

CREATING A PLOT WITH MATPLOTLIB ANNOTATIONS
```````````````````````````````````````````
# Data
x = [1,2,3,4,5]
y = [2,3,4,7,11]
# creating a plot with annotations
plt.plot(x, y)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Plot with annotations')
plt.annotate('Peak', xy = (5,11), xytext = (4,10), 
              arrowprops = dict(facecolor = 'black', shrink = 0.05))
plt.show()

``````````````````````````````````````````````````````````````````````````````````````````````

CREATING A SIMPLE LINE PLOT WITH SEABORN
````````````````````````````````````````````
import seaborn as sns
import matplotlib.pyplot as plt
# Data
x = [1,2,3,4,5]
y = [2,3,4,7,11]
# creating a line plot
sns.lineplot(x=x, y=y)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Simple Line Plot')
plt.show()

CREATING A SIMPLE BARPLOT USING SEABORN
# Data
products = ["Pc", "TV", "REF", "Micro"]
sales = [2,3,4,7]
# creating a scatter plot
sns.barplot(x=products, y=sales, color = "r", width/height = 0.1)
plt.xlabel('Products')
plt.ylabel('sales (in 1000s)')
plt.title('Simple Bar Plot')
plt.show()

CREATING A SIMPLE HISTOGRAM WITH SEABORN
````````````````````````````````````````````
# Data
data = [1,2,2,3,3,3,4,4,4,4]
# creating a line plot
sns.histplot(data, bins = 4)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Simple Histogram')
plt.show()

CREATING A PAIRPLOT WITH SEABORN
`````````````````````````````````
import seaborm as sns
import matplotlib.pyplot as plt
from sklearn.datasets import load_iris
iris = load_iris()
iris_data = sns.load_datasets("iris")
# Creating a pair plot
sns.pairplot(iris_data, hue = 'species')
plt.title('Pair Plot with seaborn')
plt.show()

CREATING A HEATMAP WITH SEABORN
```````````````````````````````
import numpy as np
#data
data = np.random.rand(10,12)
sns.heatmap(data)
plt.title('Heatmap with Seaborn')
plt.show()