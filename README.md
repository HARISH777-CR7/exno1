# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output

 ````python
     import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import  SAMPLEIDS.csv as df
df=pd.read_csv("SAMPLEIDS.csv")
print(df)
```` 
![alt text](<Screenshot 2025-10-07 113351.png>)
````python
df.head()
````
![alt text](<Screenshot 2025-10-07 113405 - Copy.png>)
````python
df.tail()
 ````

 ![alt text](<Screenshot 2025-10-07 113405.png>)

````python
df.describe()
````

![alt text](<Screenshot 2025-10-07 113429.png>)
````python
df.columns
````
![alt text](<Screenshot 2025-10-07 113440.png>)
````python
df.dtypes
````
![alt text](<Screenshot 2025-10-07 113447.png>)

````python
df.info()
````
![alt text](<Screenshot 2025-10-07 113503.png>)
````python
df.nunique()
````
![alt text](<Screenshot 2025-10-07 113534.png>)
````python
df.isnull()
````
![alt text](<Screenshot 2025-10-07 113543.png>)
````python
df["M3"]
````
![alt text](<Screenshot 2025-10-07 113557.png>)
````python
df["M3"].fillna("gowk",inplace=True)
 print(df)
````
![alt text](<Screenshot 2025-10-07 113631.png>)

````python
 df.drop(["M4"],axis=1,inplace=True)
 print(df)
 ````
 ![alt text](<Screenshot 2025-10-07 113659.png>)

 ````python

 sus=df.groupby("GENDER")
hh=sus["GENDER"].count()
print(hh)
````
![alt text](<Screenshot 2025-10-07 113709.png>)
````python
plt.figure(figsize=(8,5))
sns.barplot(x="GENDER",y="TOTAL",data=df,color='black',edgecolor='red')
plt.title("GENDER VS MARKS")
 

 
plt.show()
 ```` 
 ![alt text](<Screenshot 2025-10-07 113734.png>)

````python
plt.figure(figsize=(8,5))
sns.histplot(df['GENDER'],bins=10,color='black')
````
![alt text](<Screenshot 2025-10-07 113750.png>)
````python

sns.scatterplot(x='',y='TOTAL',data=df)
````
![alt text](<Screenshot 2025-10-07 113802.png>)
````python
sns.lineplot(x='M1',y='TOTAL',data=df)
````
![alt text](<Screenshot 2025-10-07 113814.png>)

# Result
         sucessfull
