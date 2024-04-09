
1.  Load the data from a opened google sheet
```
df = pd.DataFrame.from_records(rows)
```
2.  Load the data from a csv file

```
pd.read_csv('filename')
```

3. Assigning the first row of the dataframe to be the data headers
```
df.columns =  df.iloc[0]
# to prevent duplication of the header rows slice the first row
df = df[1:]
```

4. To replace a values into something else for example in column whose header is "words" where the values 'alc' is to be replaced with 'Alc'
```
replace_dict = {'alc':'Alc'}
df["words"] = df["word"].replace(replace_dict)
```


5. to display a whole dataframe in google colab
```
display(df)
```

6. To split a column into new columns. For example If the column 'hospital|hos_code' where columns values are of the form 'xyzHosp|4321'  and the new column names are to be "Hosp" and 'hosp_code' then
```
df[['Hosp','hosp_code']] = df['hospital|hos_code].str.split('|',expand=True)
```

7. To create a conditional column based on the comparison between two existing columns. For example let there be 2 columns 'x' and 'y' and a new column 'z' is to be created with values 'Yes' if corresponding values are equal in 'x' and 'y' and 'No' if they DONT match..

```
import pandas pd
import numpy as np

# create the new column with dummy values
df['z'] = 'unknown'

# then use numpy where function
df['z'] = np.where(df['x'] == df['y'], "Yes", "No")
```

8. merge two dataframes based on a column. Eg let there be 2 dataframes 'df1' and 'df2' and the dataframes are to be merged based on a common column 'id', then. (This will retain all the rows in the df1 dataframe)
```
df3 = df1.merge(df2,how='left',on='id')
```

9. To alter the column order. For example the let the dataframe df1 contain the columns 'a','b' and 'c' in that order. Now if the column order need to be 'c' , 'b' and 'a' do the following
```
# create a new list with the desired column order
new_col_order = ['c','b','a']
df1 = df1[new_col_order]
```
10. To save the dataframe to a csv file.
```
df.to_csv('path to file')
```
