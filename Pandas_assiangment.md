```python
Pandas_assiangment
Q1. How do you load a CSV file into a Pandas DataFrame?

Ans: pd.raed_csv("FileName.csv")

Q2. How do you check the data type of a column in a Pandas DataFrame?

Ans: To check the data type of a column in a Pandas DataFrame, you can use the "dtypes" attribute of the DataFrame. This attribute returns a Pandas Series object containing the data type of each column in the DataFrame. Eg: df.dtypes["column_name"] Alternatively,We can use the info() method of the DataFrame to get a summary of the data types of all the columns in the DataFrame.

Q3. How do you select rows from a Pandas DataFrame based on a condition?

Ans: To select rows from a Pandas DataFrame based on a condition, We can use the 'loc' method, which allows you to select rows by labels or by Boolean conditions.

Q4. How do you rename columns in a Pandas DataFrame?

Ans: To rename columns in a Pandas DataFrame, you can use the " rename() " method. This method allows you to specify the new names for one or more columns by providing a mapping of old column names to new column names. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

rename columns 'A' and 'B' to 'C' and 'D'
df = df.rename(columns={'A': 'C', 'B': 'D'})

Q5. How do you drop columns in a Pandas DataFrame?

Ans: To drop columns in a Pandas DataFrame, We can use the " drop() " method. This method allows you to specify which columns you want to drop by providing a list of column names or a sequence of column names. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

drop columns 'A' and 'C'
df = df.drop(columns=['A', 'C'])

Q6. How do you find the unique values in a column of a Pandas DataFrame?

Ans: To find the unique values in a column of a Pandas DataFrame, you can use the "unique()" method of the column. This method returns an array containing the unique values in the column. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3, 2, 3, 1], 'B': [4, 5, 6, 5, 6, 4]})

find the unique values in column 'A'
unique_values = df['A'].unique()

print the unique values
print(unique_values)

Q7. How do you find the number of missing values in each column of a Pandas DataFrame?

Ans: To find the number of missing values in each column of a Pandas DataFrame, We can use the "isnull()" method of the DataFrame. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3, None], 'B': [4, None, 6, None], 'C': [None, 8, 9, 10]})

find the number of missing values in each column
missing_values = df.isnull().sum()

print the number of missing values in each column
print(missing_values)

Q8. How do you fill missing values in a Pandas DataFrame with a specific value?

Ans: To fill missing values in a Pandas DataFrame with a specific value, we can use the "fillna()" method of the DataFrame. This method allows you to replace missing values in the DataFrame with a specified value. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3, None], 'B': [4, None, 6, None], 'C': [None, 8, 9, 10]})

fill missing values with 0
df = df.fillna(0)

Q9. How do you concatenate two Pandas DataFrames?

Ans: To concatenate two Pandas DataFrames, We can use the "concat()" function from the Pandas library. This function allows you to combine the rows or columns of two or more DataFrames into a single DataFrame. Eg: import pandas as pd

create two sample DataFrames
df1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]}) df2 = pd.DataFrame({'A': [7, 8, 9], 'B': [10, 11, 12]})

concatenate the DataFrames along the rows
df = pd.concat([df1, df2])

Q10. How do you merge two Pandas DataFrames on a specific column?

Ans: To merge two Pandas DataFrames on a specific column,We can use the " merge() " function from the Pandas library. This function allows you to join the rows of two DataFrames based on the values in a specified column. Eg: import pandas as pd

create two sample DataFrames
df1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]}) df2 = pd.DataFrame({'C': [7, 8, 9], 'B': [4, 5, 6]})

merge the DataFrames on column 'B'
df = pd.merge(df1, df2, on='B')

Q11. How do you group data in a Pandas DataFrame by a specific column and apply an aggregation function?

Ans: To group data in a Pandas DataFrame by a specific column and apply an aggregation function,We can use the "groupby()" method of the DataFrame and the "agg()" method of the resulting GroupBy object. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3, 1, 2, 3], 'B': [4, 5, 6, 4, 5, 6]})

group the DataFrame by column 'A' and apply the sum() function to column 'B'
df = df.groupby('A')['B'].agg('sum')

Q12. How do you pivot a Pandas DataFrame?

Ans: To pivot a Pandas DataFrame, We can use the "pivot()" method of the DataFrame. This method allows you to reshape the DataFrame by pivoting its columns into rows and its rows into columns. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3, 1, 2, 3], 'B': [4, 5, 6, 4, 5, 6], 'C': [7, 8, 9, 7, 8, 9]})

pivot the DataFrame
df = df.pivot(index='A', columns='B', values='C')

Q13. How do you change the data type of a column in a Pandas DataFrame?

Ans: To change the data type of a column in a Pandas DataFrame, you can use the "astype()" method of the column. This method allows you to specify the new data type for the column by providing the data type as a string or as the corresponding Python data type. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': ['4', '5', '6']})

change the data type of column 'B' to integer
df['B'] = df['B'].astype(int)

Q14. How do you sort a Pandas DataFrame by a specific column?

Ans: To sort a Pandas DataFrame by a specific column, you can use the "sort_values()" method of the DataFrame. This method allows you to specify the column you want to sort by, as well as the sorting order (ascending or descending). Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [3, 2, 1], 'B': [6, 5, 4]})

sort the DataFrame by column 'A' in ascending order
df = df.sort_values('A')

Q15. How do you create a copy of a Pandas DataFrame?

Ans: To create a copy of a Pandas DataFrame, you can use the "copy()" method of the DataFrame. This method returns a new DataFrame object that is a copy of the original DataFrame. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

create a copy of the DataFrame
df_copy = df.copy()

Q16. How do you filter rows of a Pandas DataFrame by multiple conditions?

Ans: To filter rows of a Pandas DataFrame by multiple conditions, We can use the & and | operators to combine multiple Boolean expressions. These operators allow you to combine the conditions using the logical AND and OR operators, respectively. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3, 4, 5], 'B': [6, 7, 8, 9, 10]})

filter the DataFrame using multiple conditions
df = df[(df['A'] > 2) & (df['B'] < 9)]

Q17. How do you calculate the mean of a column in a Pandas DataFrame?

Ans: To calculate the mean of a column in a Pandas DataFrame, We can use the "mean()" method of the column. This method returns the arithmetic mean of the values in the column, which is the sum of the values divided by the number of values. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

calculate the mean of column 'A'
mean = df['A'].mean()

Q18. How do you calculate the standard deviation of a column in a Pandas DataFrame?

Ans: To calculate the standard deviation of a column in a Pandas DataFrame,We can use the " std() " method of the column. This method returns the standard deviation of the values in the column, which is a measure of the spread or dispersion of the values. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

calculate the standard deviation of column 'A'
std = df['A'].std()

Q19. How do you calculate the correlation between two columns in a Pandas DataFrame?

Ans: To calculate the correlation between two columns in a Pandas DataFrame, We can use the " corr() " method of the DataFrame. This method calculates the Pearson correlation coefficient between the two columns, which is a measure of the linear relationship between the values in the columns. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

calculate the correlation between columns 'A' and 'B'
corr = df['A'].corr(df['B'])

Q20. How do you select specific columns in a DataFrame using their labels?

Ans: To select specific columns in a DataFrame using their labels, We can use the "loc[]" method of the DataFrame. This method allows you to specify the labels of the columns you want to select, as well as the labels of the rows you want to include in the selection. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

select columns 'A' and 'C'
df = df.loc[:, ['A', 'C']]

Q21. How do you select specific rows in a DataFrame using their indexes?

Ans: To select specific rows in a DataFrame using their indexes, We can use the "iloc[]" method of the DataFrame. This method allows us to specify the indexes of the rows you want to select, as well as the indexes of the columns you want to include in the selection. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

select rows with index 1 and 2
df = df.iloc[[1, 2], :]

Q22. How do you sort a DataFrame by a specific column?

Ans: To sort a DataFrame by a specific column,We can use the " sort_values() " method of the DataFrame. This method allows us to specify the column you want to sort by, as well as the sorting order (ascending or descending). Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [3, 2, 1], 'B': [6, 5, 4]})

sort the DataFrame by column 'A' in ascending order
df = df.sort_values('A')

Q23. How do you create a new column in a DataFrame based on the values of another column?

Ans: To create a new column in a DataFrame based on the values of another column, We can use the "apply()" method of the DataFrame. This method allows us to specify a function that will be applied to each value in the column, and the result of the function will be used to populate the new column. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

create a new column 'C' based on the values in column 'A'
df['C'] = df['A'].apply(lambda x: x * 2)

Q24. How do you remove duplicates from a DataFrame?

Ans:To remove duplicates from a DataFrame, We can use the "drop_duplicates()" method of the DataFrame. This method returns a new DataFrame that contains only the unique rows from the original DataFrame. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 2, 3, 3, 3], 'B': [4, 5, 5, 6, 6, 6]})

remove duplicates from the DataFrame
df = df.drop_duplicates()

Q25. What is the difference between .loc and .iloc in Pandas?

Ans: The loc and iloc methods are used to select rows and columns in a Pandas DataFrame. The difference between these two methods is the way they select the data:

loc: This method uses the labels of the rows and columns to select the data. This means that you can use the actual names or labels of the rows and columns to specify the data you want to select. iloc: This method uses the indexes of the rows and columns to select the data. This means that you can use the numerical positions of the rows and columns to specify the data you want to select. Eg: import pandas as pd

create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

select the first row using 'loc'
print(df.loc[0, :])

select the first row using 'iloc'
print(df.iloc[0, :])

```
