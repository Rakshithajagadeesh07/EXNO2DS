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
```
import pandas as pd
import seaborn as sns
df=pd.read_csv('titanic_dataset.csv')
df
```

<img width="663" height="420" alt="image" src="https://github.com/user-attachments/assets/0573c007-5d36-4387-8d07-0c7839823abc" />

```
df.shape
```
<img width="130" height="57" alt="image" src="https://github.com/user-attachments/assets/2a4c394c-6276-428a-a32a-3a3c0eeb161d" />

```
df.set_index("PassengerId",inplace=True)
df
```

<img width="660" height="387" alt="image" src="https://github.com/user-attachments/assets/1025c18a-23b4-46aa-a487-bef241199420" />



```
df.nunique()
```
<img width="331" height="353" alt="image" src="https://github.com/user-attachments/assets/1cac0a1f-5a5d-467e-9d30-27e8671eeca3" />

```
df.rename(columns={"Sex":"Gender"},inplace=True)
df
```
<img width="658" height="380" alt="image" src="https://github.com/user-attachments/assets/2bcc7484-cd7e-4e40-a79c-65923016c5fb" />

```
import seaborn as sns
sns.countplot(data=df)
```

<img width="571" height="413" alt="download" src="https://github.com/user-attachments/assets/b5900b64-6f1b-44c4-93a7-631618a65e11" />

```
sns.countplot(x="Survived",hue="Gender",data=df)
```
<img width="571" height="432" alt="download" src="https://github.com/user-attachments/assets/c52911a9-d725-450b-8e67-320bb585a217" />

```
sns.catplot(x="Survived",hue= "Gender", y='Fare',data=df,kind="box")
```

<img width="582" height="490" alt="download" src="https://github.com/user-attachments/assets/54d24932-062a-4798-b76f-51a7688e5887" />

```
sns.catplot(x="Survived",hue= "Gender", data=df,kind="count")
```
<img width="582" height="489" alt="download" src="https://github.com/user-attachments/assets/4b0eb83f-26b0-4ae9-b587-020ab21629c5" />

```
sns.boxplot(data=df)
```

<img width="552" height="413" alt="download" src="https://github.com/user-attachments/assets/1edaabb0-51d3-4fc3-b5cc-9c4cb8e54787" />

```
df.boxplot(column="Survived" , by= "Gender")
```

<img width="563" height="461" alt="download" src="https://github.com/user-attachments/assets/d7a75a91-1b2b-42bb-af19-59dfc8984b32" />

```
sns.scatterplot(data=df)
```

<img width="552" height="432" alt="download" src="https://github.com/user-attachments/assets/277d0059-ce5e-485d-b095-806c4bed4f0a" />

```
sns.scatterplot(x=df['Age'],y=df['Fare'])
```

<img width="571" height="432" alt="download" src="https://github.com/user-attachments/assets/d86cc175-f6b3-4e23-824f-41befee4889c" />

```
sns.jointplot(x='Age' , y ='Fare' , data=df)
```
<img width="594" height="590" alt="download" src="https://github.com/user-attachments/assets/fc3750ae-d88b-4f24-8671-6391715078d3" />

```
sns.jointplot(x='Age',y='Fare',data=df,kind="kde")
```
<img width="594" height="590" alt="download" src="https://github.com/user-attachments/assets/0967676f-ef88-4a86-9dd6-395ca22f4ad6" />

```
sns.jointplot(x='Age',y='Fare',data=df,kind='hist')
```
<img width="594" height="590" alt="download" src="https://github.com/user-attachments/assets/4835edd6-342e-4833-9dc2-3a7add497d06" />

```
sns.pairplot(data=df)
```
<img width="1476" height="1476" alt="download" src="https://github.com/user-attachments/assets/1f01d17e-1e02-4463-a3e9-1a86c3b9249b" />

```
corr1=df.select_dtypes(include=['number']).corr()
sns.heatmap(corr1 , annot=True)
```
<img width="527" height="418" alt="download" src="https://github.com/user-attachments/assets/9ec0dcc8-d0f7-487c-b1b1-3799eb776449" />


# RESULT
All conditions are execute Successfully
