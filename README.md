# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE 
# DATA SET
```
import pandas as pd
df=pd.read_csv("/content/Data_set intro to ds.csv")
print(df)

df.head(5)

df.info()

df.isnull()

df.isnull().sum()

df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()

df.isnull().sum()
```
# LOAN DATA
```
import pandas as pd
df=pd.read_csv("/content/Loan_data intro to ds.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()


df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())

df.info()
df.isnull().sum()
```
# OUTPUT
## DATA SET

![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/d57cef4c-eb8f-47d8-9c74-0fe955e412d4)

![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/4df8c8f4-48ea-4ccc-abb9-5ee744566dd4)

![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/36d378d3-7fe4-4017-9d5e-8d12802d1426)

![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/19206b90-3425-4307-8c8d-f32f0baa677e)


## LOAN DATA

![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/242baa95-a94a-4091-a32d-71603314b3ce)

![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/bbbe9dfd-f950-4b22-b0b9-4e3581f49a05)


![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/8367be8b-d346-4537-850a-6cd85b7161cc)

![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/130095a5-0d73-4725-b160-9c6c351f93fd)


![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/b502e6fc-d92f-431f-9dd8-58e5f8e2c262)


