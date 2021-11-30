#pandas
##  import pandas
import pandas as pd
    this is industry standard to import pandas as pd        


## create a Series:

## reading a csv
variable_df = pd.read_csv(csv file)

## Creating a data frame:
variable = pd.DataFrame(input)

## Return data
### return all data
variable
### return the top or bottom 5
variable.head()
variable.tail()

## count data
### in each column
variable.count()
variable["column header"].count()

## Perform sum on column
variable["column"].sum()

### null values
variable.isnull() returns true/false for each cell
variable.isnull().sum: will sum up the non-null values

### non-null values
variable.notnull()
variable.notnull().sum


## Deal with  missing values
variable.fillna(<WHAT TO FILL DATA WITH>)
variable.dropna()
** Caution when dealing with missing values as may have an affect on your future analysis**

## Find Data types of columns
variable.dtype
variable.columnHeader.dtype
variable["column header with space"]

## Add column data to a list
variable2 = variable["column_name"].tolist()
converts a column in the data frame into a list

## Split
variable.split()
len(variable.split()) = how many "words" there are separated by spaces
to call a specific element in the string, use something like variable.split()[2]

## Returning unique items in a list
set(variable)
returns all the unique items in a list, sorted alphabetically if strings

## return unique value
variable.unique()
len(variable.unique())
variable["column_header"].unique()

## Strip values - anything in the parenthesis
variable.strip("string"))
** Learn more about this - may cause unintended consequences**

## replace values: 
replace old value with new value
variable.replace("old value", "new value")
*can only be used on python strings, will not work on objects

## Converting data to string
variable_df["column_header"].str.replace()

## Merge dataframes
pd.merge(df1, df2, on=["merge_column_df1", "merge_column_df2"])

## Calculatng Averages
variable["column_header"].mean()

## Formatting with map()
function
used for substituting each value in a series with another value, where the new value is generated from function, dictionary or a series
variable.map("current_value_1" : "new_value_1",  "current_value_2" : "new_value_2", etc)

## format function
used to specify format ex. decimal places, thousands separator
"{value:format specification}".format(value)
value = value to format - sometimes this is no need to put this because it is implied elsewhere
format specification = how it will be formatted
ex. {:0f}.format(variable)
0 = zero decimal places, could change to any number for the # decimal places needed
f = floating point decimal

## Change Column Order
column_order = ['column3', 'column1', column5]
dataframe = dataframe[column_order]


## set specific column as index
new_variable = dataframe_variable.set_index(["column_to_be_index"])["column_to_be_series"]

## Value_counts()
method returns a series of data with the # of times a value appears in a specificed row
new_series = dataframe_varial["column_to_count"] --> will count how up how many times values appear
will put the index as the different values, series will be sum of how many times the value appears in the data
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.value_counts.html

## Group By
will split an object (like a dafaframe), apply math operations and combine the result
ex. series = data_frame_variable.gropuby(["column_Header_to_groupby"]).mean()["column_to_perform_calclation]
if nothing in the mean, it will perform the math operaton on all the columns it can (ex. with int, float)
Will set the index as the "Column_header_to_groupby"

Multiple variables in groupby:
new_df = df.groupby(['column1', 'column2'])

https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.groupby.html

## Sort the data
sort_values(["Column_header], asending=False)
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sort_values.html

## Describe the data 
describe()  method
dataframe.describe()
can apply to dataframe or series to return descriptive stats
    The number of rows in the DataFrame or Series as count
    The average of the rows as mean
    The standard deviation of the rows as std
    The minimum value of the rows as min
    The 25th percentile as 25%
    The 50th percentile as 50%
    The 75th percentile as 75%
    The minimum value of the rows as max

## Cut the data
segments and sorts data values into bins
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.cut.html

## Adding a legent
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.legend.html
https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.legend.html
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.text.html
