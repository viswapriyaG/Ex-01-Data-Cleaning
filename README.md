# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.
# DATE:

GITHUB LINK:https://github.com/viswapriyaG/Ex-01-Data-Cleaning.git

COLAB LINK:https://colab.research.google.com/drive/1rjdXCtvdwa5lYRahrCAftfrXhbWgsECJ#scrollTo=HwSJ33pYbHdK

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

Program developed by: VISWA PRIYA G

Register number: 212221220061
```
import pandas as pd

import numpy as np

import seaborn as sns

df1 = pd.read_csv("Data_set.csv")

df1

df1.head()

df1.describe()

df1.info()

df1.tail()

df1.shape

df1.columns

df1.isnull().sum()

df1.duplicated()

#Using mode method to fill the data in columns as Object(String)
#mode()[0] - Takes the most reccuring value and fills the empty cells
df1['show_name'] = df1['show_name'].fillna(df1['show_name'].mode()[0])
df1['aired_on'] = df1['aired_on'].fillna(df1['aired_on'].mode()[0])
df1['original_network'] = df1['original_network'].fillna(df1['original_network'].mode()[0])

sns.boxplot(x="rating",data=df1)

#Using mean method to fill the data
df1['rating'] = df1['rating'].fillna(df1['rating'].mean())
df1['current_overall_rank'] = df1['current_overall_rank'].fillna(df1['current_overall_rank'].mean())
df1['watchers'] = df1['watchers'].fillna(df1['watchers'].mean())

#Checking the total no.of null values again
df1.isnull().sum()

#Checking info of the dataset to check all the columns have entries
df1.info()
```
# OUPUT
## DATASET

![image](https://user-images.githubusercontent.com/127847210/228211764-e9eb9604-43e8-4529-bb33-aa8edfaab9de.png)


## HEAD

![image](https://user-images.githubusercontent.com/127847210/228211864-d2a94905-2748-4a41-943e-dad1a7a5a323.png)

## DESCRIBE

![image](https://user-images.githubusercontent.com/127847210/228211941-002cefe2-7c3b-4e3c-8b2a-bbe255583f6a.png)


## INFO

![image](https://user-images.githubusercontent.com/127847210/228212033-5940bfde-4d20-4f84-a933-086e60358d2c.png)


## TAIL

![image](https://user-images.githubusercontent.com/127847210/228212236-d07fbf13-9d4a-44f1-a2c7-4ef7158eb1c3.png)


## SHAPE

![image](https://user-images.githubusercontent.com/127847210/228212343-f8eb0322-e56c-41e5-8a5f-fd9ecfe8c019.png)

## isnull().sum() - Pre Cleaning

![image](https://user-images.githubusercontent.com/127847210/228212465-efd287f9-0734-482e-91c2-d0f15650d6db.png)

## DUPLICATES

![image](https://user-images.githubusercontent.com/127847210/228212560-e5600b9c-3bfd-4e91-b2c4-c0e09df01462.png)


## SNS PLOT-RATING

![image](https://user-images.githubusercontent.com/127847210/228213897-5fb68eac-b302-44d6-877f-4eb6e37b678c.png)


## isnull().sum() - Post Cleaning

![image](https://user-images.githubusercontent.com/127847210/228214005-bf27536c-932a-4eaf-bcbe-29d94039e0a0.png)


## Info - Post Cleaning

![image](https://user-images.githubusercontent.com/127847210/228214232-bb8f6dd2-3bd9-4489-a6ca-c248148a0df0.png)


# Result:
The given data is read and data cleaning is performed and the cleaned data is saved to a file.
