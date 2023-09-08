# Ex-01_DS_Data_Cleansing

# AIM
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
## For Data_Set
```
import pandas as pd
df=pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
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
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```
## For Loan_Data
```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
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
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```

# OUTPUT
## For Data_Set
### Data:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/ad97c053-09d2-4603-a421-b91d4ea5e2fb)
### Non Null Before:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/d03bd90e-6927-40d7-a6a4-25064bb3b8f6)
### Mode:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/285df8ff-5c5e-497b-8cb8-f7d7c47f3d84)
### Median:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/b1fabb4c-08d4-497d-85fe-9484870c978b)
### Non Null After:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/d57eb7b7-97e1-4dbf-b9bb-35c528ea94a2)

## For Loan_Data
### Data:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/bf93da88-0eab-423f-9742-35cc23fa040e)
### Non Null Before:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/68e7f450-0d03-4f7e-979d-13e5d1c90a27)
### Mode:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/dc8b32ba-5cbc-44d8-aae3-5cb7c14fbfae)
### Mean:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/cd57f782-e243-4a7a-8640-9b260d44dd54)
### Median:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/7c211cac-753e-4e4d-8990-292e8caa9d7d)
### Non Null After:
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex01/assets/121166075/04cf35d9-74f2-43ea-adb4-0e7c11dc6487)

# Result:
Thus,the given data is read,cleared and the cleaned data is saved into the file.


