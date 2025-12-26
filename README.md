# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT

     import pandas as pd df=pd.read_csv("C:\Users\admin\Downloads\titanic_dataset.csv") df
<img width="1430" height="623" alt="image" src="https://github.com/user-attachments/assets/6581692a-f8a2-4943-b61b-febac7936e64" />
df.shape
<img width="1327" height="84" alt="image" src="https://github.com/user-attachments/assets/c04e9b6c-da29-47ee-b19c-82dfda5e8262" />
df.set_index("PassengerId",inplace=True) df
<img width="1323" height="587" alt="image" src="https://github.com/user-attachments/assets/b6338997-7e05-4b31-86ff-95e0efd0488f" />
df.unique()
<img width="1147" height="314" alt="image" src="https://github.com/user-attachments/assets/b806d85e-0b95-4a5f-9a5e-e46365be9428" />
df['Survived'].value_counts() 
<img width="1191" height="134" alt="image" src="https://github.com/user-attachments/assets/88a10ed4-4c7f-4634-ae3d-1cfeef7d2eef" />
df.Pclass.unique() 
<img width="1216" height="81" alt="image" src="https://github.com/user-attachments/assets/164cdcde-6e48-4e57-b5c7-2ef363f7f3b7" />
df.rename(columns={"Sex":"Gender"},inplace=True) df 
<img width="1333" height="587" alt="image" src="https://github.com/user-attachments/assets/25c64656-0aa8-43c0-a61f-3b82366a100f" />
import seaborn as sns sns.countplot(data=df)
<img width="1376" height="674" alt="image" src="https://github.com/user-attachments/assets/594e3871-e807-41d9-b983-91f1edb3507e" />
sns.countplot(x="Survived",hue="Gender",data=df)
<img width="1167" height="637" alt="image" src="https://github.com/user-attachments/assets/c103002d-a9ae-476a-adb5-73cf608fb722" />
sns.catplot(x="Survived",hue="Gender",data=df,kind="count")
<img width="1290" height="704" alt="image" src="https://github.com/user-attachments/assets/ffe32d7c-7e44-4d2d-b4cd-125f93d479e9" />
sns.boxplot(data=df) 
<img width="1045" height="621" alt="image" src="https://github.com/user-attachments/assets/26c17997-274b-4bd3-9685-1e9efa8942b4" />
df.boxplot(column="Survived",by="Gender") 
<img width="1148" height="658" alt="image" src="https://github.com/user-attachments/assets/e8f877d5-e0ca-4cf1-868d-9ea867cb975c" />
sns.scatterplot(data=df) 
<img width="1393" height="646" alt="image" src="https://github.com/user-attachments/assets/2e7bf2e3-a9e4-42cc-9995-fe116c896af6" />
sns.scatterplot(x=df['Age'],y=df['Fare'])
<img width="1389" height="645" alt="image" src="https://github.com/user-attachments/assets/1b84ba1d-3a97-4fc3-9f4f-9cdbd6fdb841" />
sns.jointplot(x='Age',y='Fare',data=df,kind='kde')
<img width="1315" height="822" alt="image" src="https://github.com/user-attachments/assets/143cab42-5177-4efd-a2b2-b38e614479b8" />
sns.jointplot(x='Age',y='Fare',data=df,kind='hist')
<img width="1387" height="839" alt="image" src="https://github.com/user-attachments/assets/4d14a522-c698-4ead-9e1a-764835d1764d" />



        
     









# RESULT
            The EDA process has been done successfully
