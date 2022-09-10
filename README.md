# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Data_set.csv")
print(df)
df.head(5)
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()

```
# OUPUT
![image](https://user-images.githubusercontent.com/94165327/189481666-9556ab0e-b48f-4df5-a0a2-efacb4ffa863.png)


![image](https://user-images.githubusercontent.com/94165327/189481679-ff83203f-12cb-4512-93d4-8cf5e37b21b2.png)

![image](https://user-images.githubusercontent.com/94165327/189481700-c16cc6ab-1dd2-4a5c-9b26-de8bd450e1ee.png)
df.head()
![image](https://user-images.githubusercontent.com/94165327/189481717-a49aca91-ab9e-40a3-8a64-a882815cb4e0.png)

df.head()
![image](https://user-images.githubusercontent.com/94165327/189481725-e0fcca6e-64e2-42af-906e-f33ba5fa92cc.png)

df.info()
![image](https://user-images.githubusercontent.com/94165327/189481750-26b886fc-6e59-4cb4-895b-5e29b2fa25c1.png)

df.isnull().sum()
![image](https://user-images.githubusercontent.com/94165327/189481757-9026c499-2492-430b-8796-03257b346dc2.png)

