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
## FOR DATA SET
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/bbf7faa9-7582-44f0-96d9-a5af285e8870)
## NON NULL BEFORE
```
df.info()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/639a9ae6-1444-4ad2-840e-39b1ecf41195)

```
df.head(5)
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/e9c3f41c-db7a-4ad3-ae5d-489e9f1c7cbd)
```
df.isnull()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/384cc4fe-61a5-4e78-9626-939f20aaa0f0)
```
df.isnull().sum()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/36802828-8baa-409a-884d-d9548bfe6033)

## MEAN
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/c0db037e-27ea-4dbe-8dfe-d73e3f8a2ec8)

## MEDIAN
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/69d76713-4a53-46de-9bb4-09962fec4486)

## MODE
```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/38a78333-fc45-4b30-b16d-2ccc9c28e98e)

## NON NULL AFTER 
```
df.info()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/5d78718a-92e4-4857-9497-b606a56b1ac4)

```
df.isnull().sum()
```

![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/bc297ca0-03a9-446b-abf7-463374049be5)



## FOR LOAN DATA
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/3728de91-ad0f-40fb-aa90-ca87c69f0373)
```
import pandas as pd
df=pd.read_csv("/Loan_data intro to ds.csv")
print(df)
df.head(10)
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/56168b3f-caa7-476e-8641-b401f0cd0201)
## NON NULL BEFORE
```
df.info()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/592f6ba3-b62f-4fd5-b9be-1c9d33f204b9)
```
df.head(5)
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/fcd47fc5-6063-40b4-ab06-e678c2c08623)
## MEAN
```
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/0dcde8ae-1742-4fa7-95bd-7bc92e48edd9)

## MEDIAN
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/94277061-c5b0-48ec-932e-f0a2ac315eab)

## MODE
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/0b6c753f-56bb-4b9a-885c-ebf0fb84a85b)

## NON NULL AFTER
```
df.info()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/76d21580-d5d5-4de6-8709-f54b3a3313de)
```
df.isnull()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/cf65e122-8746-4e7d-b0bf-fb92e504f0a5)

```
df.isnull().sum()
```
![image](https://github.com/SRINIDHISENTHILNATHAN/ODD2023-Datascience-Ex01/assets/121373170/a6a9bb8b-757e-4cab-bfe0-4c00ff387c64)

# RESULT

Thus,the given data is read,cleansed and the cleaned data is saved into the file.







