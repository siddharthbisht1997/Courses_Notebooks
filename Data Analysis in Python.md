*These notes have been taken from the course Data Analysis in Python by Cognitive Class.*

#### Data Acquisation
It is the process of loading and reading data into notebook from various sources. One of the most useful libraries for Data Handling is Pandas. It offers a lot of features and functions to handle, access and work with Data.

##### Importing the Pandas Library

```python
import pandas as pd
```
##### Reading from File

```python
path_to_file = "Could be a URL Link(This link should return the file object and not html page) or the address of the File on the Disk"
df = pd.read_csv(path_to_file)
```
Here *df* is the DataFrame object. 

##### Changing the Column Names

There are features to add the column names while reading, or one could omit the header. They can also be added at a later stage using the following command.
```python
header = ['List of all Column Names']
df.columns = header
```

##### Taking a look at the data
```python
n = "number of rows you want to see, must be an interger, 5 is the default value"
df.head(n) # First n rows
df.tail(n) # Last n rows
```

##### Saving and Reading different Formats

|Format|Read|Save|
----|----|----
|CSV|pd.read_csv("path")|df.to_csv("path of saving location")|
|JSON|pd.read_json("path")|df.to_json("path of saving location"|
|EXCEL|pd.read_excel("path")|df.to_excel("path of saving location"|
|SQL|pd.read_sql("path")|df.to_sql("path of saving location"|

##### Important Methods and Tools

|Command|Use|
----|----
|df.dtypes| Returns the list of Datatypes of the columns in the Dataframe|
|df.describe()*| Returns a statistical summary, for every column returns the count,mean, standard deviation, max value, min value, Q1, Q2, Q3|
|df.info()|Top 30 and Bottom 30 rows of the dataframe|


*\*By default, describe method does not show the categorical columns. To include all the columns use the argument **include = "all"** inside the describe method. Adding features like Unique, frequency etc.*
