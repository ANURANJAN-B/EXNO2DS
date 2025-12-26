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
        <img width="1430" height="623" alt="image" src="https://github.com/user-attachments/assets/b23ba353-2dd2-480b-b308-c43811d8dee9" />
        df.shape
        <img width="1327" height="84" alt="image" src="https://github.com/user-attachments/assets/a6953079-6f2b-4b01-90c1-932c06bc43ad" />
        df.set_index("PassengerId",inplace=True) df 
        <img width="1323" height="587" alt="image" src="https://github.com/user-attachments/assets/74d3fb82-07ea-49cb-8596-e78d4e6d4f54" />
        df.unique()
        <img width="1147" height="314" alt="image" src="https://github.com/user-attachments/assets/c625688a-94df-4209-bad5-63be488ddd80" />
        df['Survived'].value_counts() 
        <img width="1191" height="134" alt="image" src="https://github.com/user-attachments/assets/cc35b3bf-6f0d-4af7-8766-8b1c73d15f53" />
        df.Pclass.unique() 
        <img width="1216" height="81" alt="image" src="https://github.com/user-attachments/assets/db3380ce-88ad-4b83-be50-22854d857cf7" />
        df.rename(columns={"Sex":"Gender"},inplace=True) df 
        <img width="1333" height="587" alt="image" src="https://github.com/user-attachments/assets/f6c9f429-4f42-4512-971f-1d62100629d1" />
        import seaborn as sns sns.countplot(data=df) 
        <img width="1376" height="674" alt="image" src="https://github.com/user-attachments/assets/c6812118-3167-4d72-8750-c6d365a57c9d" />
        sns.countplot(x="Survived",hue="Gender",data=df)
        <img width="1167" height="637" alt="image" src="https://github.com/user-attachments/assets/d1029890-58f7-4d5d-999e-a5c67d0a1e99" />
        sns.catplot(x="Survived",hue="Gender",data=df,kind="count")
        <img width="1290" height="704" alt="image" src="https://github.com/user-attachments/assets/88a6c3d0-701a-48c4-8ea3-c6c84b44b42d" />
        sns.boxplot(data=df) 
        <img width="1045" height="621" alt="image" src="https://github.com/user-attachments/assets/5f4963e8-9ad6-4543-9fc1-4b0e24cb3165" />
        df.boxplot(column="Survived",by="Gender") 
        <img width="1148" height="658" alt="image" src="https://github.com/user-attachments/assets/7ec2a6e1-a376-40d9-9c5c-3214be34409f" />
        sns.scatterplot(data=df)
        <img width="1393" height="646" alt="image" src="https://github.com/user-attachments/assets/c92cca48-4e4e-4024-b482-bd770dd913d2" />
        sns.scatterplot(x=df['Age'],y=df['Fare'])
        <img width="1389" height="645" alt="image" src="https://github.com/user-attachments/assets/5a0cfff0-66ef-41a3-8ca9-40d2c7a61840" />
        sns.jointplot(x='Age',y='Fare',data=df,kind='kde')
        <img width="1315" height="822" alt="image" src="https://github.com/user-attachments/assets/a9a9a45b-38d9-4adc-b275-903b5075a69c" />
        sns.jointplot(x='Age',y='Fare',data=df,kind='hist')
        <img width="1387" height="839" alt="image" src="https://github.com/user-attachments/assets/e508f2eb-df7a-4e78-870d-da2027d86523" />









        
     









# RESULT
            The EDA process has been done successfully
