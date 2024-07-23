INTRIDUCTION TO PLOTLY
Definition:
Plotly: Plotly is a graphing library that makes interactive, publication-quality graphs online. It supports a wide variety of charts, including line plots, scatter plots, bar charts, 
histograms, heatmaps, and more. Plotly is particularly useful for creating interactive visualizations that can be embedded in web applications and shared online.

Key Features of Plotly
1. Interactivity: Plotly charts are interactive by default, allowing users to zoom, pan, and hover ove data points to get more information.
2. Wide Range of Chart Types: Plotly supports a variety of chart types, including basic plots, statistical plots, 30 plots, and maps.
3. Customization: Extensive options to customize the appearance and behavior of charts.
4. Integration: Easy integration with web applications and other libraries like Dash for building interactive dashboards.

LOADING DATASETS
``````````````````
import pandas as pd
# Load the dataset
df = pd.read_csv('sales_data.csv')
print(df.head())

CREATING A LINE PLOT
`````````````````````
import pplotly.express as px
# Creating a line plot
fig = px.line(df, x='Date', y='Sales', title='Sales Trend over time', markers = True)
fig.show()

CREATING A BAR CHART
`````````````````````
import pplotly.express as px
# Creating a bar chart
fig = px.bar(df, x='Date', y='Sales', title='Sales Trend over time', color='Date')
fig.show()

CREATING A SCATTER PLOT
`````````````````````
import pplotly.express as px
# Creating a scatter plot
fig = px.scatter(df, x='Date', y='Sales', title='Sales Trend over time', color='Date', size = 'Quantity', hover_data=['Product'] )
fig.show()

CREATING A BAR CHART
`````````````````````
import pplotly.express as px
# Creating a bar chart
fig = px.bar(df, x='Date', y='Sales', title='Sales Trend over time', color='Date')
fig.show()CREATING A BAR CHART
`````````````````````
import pplotly.express as px
# Creating a bar chart
fig = px.bar(df, x='Date', y='Sales', title='Sales Trend over time', color='Date')
fig.show()

CREATING A PIE CHART
`````````````````````
import pplotly.express as px
# Creating a bar chart
fig = px.pie(df, x='Date', y='Sales', title='Sales Trend over time')
fig.show()


Import plotly.express as px
# Sample data
data  = {
'City': "New York', 'Los Angeles', 'Chicago', 'Houston', 'Phoenix'], "State': ['NY', 'CA', 'IL', 'TX", "AZ'], "Population': [8419000, 3500400, 2716000, 2328000, 1650000]
}
# Creating the DataFrane
df pd.DataFrame(data)
# Create a geographical map
fig px.choropleth(df, locations State', locationmode-USA-states", color Population", scopes'usa", titles Population by State') fig.show()