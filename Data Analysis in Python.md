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
