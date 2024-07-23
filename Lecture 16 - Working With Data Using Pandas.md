#Working with Data using Pandas:

#Definition: Pandas is a powerful and flexible open-source data analysis and manipulation library for Python, provides data structures like Series (one-dimensional) and DataFrame (two-dimensional) 
#that are efficient fot handling large datasets. Pandas allows for data manipulation, aggregation, and merging.
#Use Case in Real Life: Pandas can be used in various data analysis scenarios, such as customer data analysis, financial data analysis, and marketing campaign analysis.

#CREATING A DATA FRAME FROM A DICTIONARY:

import pandas as pd
# Creating a DataFrame from a dictionary
data = {'Name':['Arjun' , 'Rohit' , 'Mohan'] , 
          'Age':[25,30,23] , 
          'City':['Mumbai' , 'Jaipur' , 'Bbsr']}
Data_Frame = pd.DataFrame(data)
print(Data_Frame)

#CREATING A DATA FRAME FROM A LIST OF DICTIONARIES:

data = [{'Name': 'Arjun', 'Age': 25, 'City': 'Mumbai'}
        {'Name': 'Rohit', 'Age': 30, 'City': 'Jaipur'}
        {'Name': 'Mohan', 'Age': 23, 'City': 'Bbsr'}]
Data_Frame = pd.DataFrame(data)
print(Data_Frame)

#CREATING A DATA FRAME FROM A CSV FILE:

# Assuming that 'data.csv' is a csv file in the current dictionary
Data_Frame = pd.read_csv('dataset.csv')
print(Data_Frame)

#DISPLAYING THE DATA

# Displaying the first few rows
print(Data_Frame.head())

# Displaying the last few rows
print(Data_Frame.tail())

# Getting the information about the DataFrame
print(Data_Frame.info())

# Descriptive Statistics
print(Data_Frame.describe())

#SELECTING COLOUMNS

# Selecting a Single coloumn
print(Data_Frame['Name'])

# Selecting Multiple coloumn's
print(Data_Frame[['Name' , 'Age']])

#SELECTING ROWS

# Selecting Rows based on Condition
print(Data_Frame[Data_Frame['Age'] > 30])

#ADDING NEW COLUMNS

# Adding a new columns
Data_Frame['Salary'] = [50000 , 25000 , 40000 , 35000 , 45000]
print(Data_Frame)

#MODIFYING EXISTING COLUMNS

# Modifying an existing column
Data_Frame['Age'] = Data_Frame['Age'] + 1
print(Data_Frame)

#DROPPING COLUMNS AND ROWS

# Dropping the Salary Column
Data_Frame = Data_Frame.drop(columns=['Salary'])
print(Data_Frame)

# Dropping a row
Data_Frame = Data_Frame.drop(index=1)
print(Data_Frame)

#GROUPING DATA

#  Grouping data by a column
grouped = Data_Frame.groupby('City')
print(groupby['Age'].mean())

#AGGREGATING DATA

# Aggregating data using multiple functions
aggregated = Data_Frame.groupby('City').agg({'Age': ['mean' , 'min' , 'max']})
print(aggregated)

#MERGING DATAFRAMES

Data_Frame1 = pd.DataFrame({'ID': [1,2,3], 'Name': ['Alice','Bob','Charile']})
Data_Frame2 = pd.DataFrame({'ID': [1,2,4], 'Salary': [50000,25000,40000]})
# Merging dataFrames on a common column
merged_df = Data_Frame1.merge(Data_Frame1, Data_Frame2, on='ID', how='inner')
print(merged_df)

#JOINING DATAFRAMES

Data_Frame1 = pd.DataFrame({'Name': ['Alice','Bob'], 'Age': [25, 30], index[0,1]})
Data_Frame2 = pd.DataFrame({'City': ['NY','LA'], index[0,2]})
# Joining dataFrames on a their index
joined_df = Data_Frame1.join(Data_Frame2, how='left')
print(joined_df)