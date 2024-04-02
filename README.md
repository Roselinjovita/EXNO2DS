
# EXNO2DS

## DEVELOPED BY:ROSELIN MARY JOVITA S
## REGISTER NUMBER:212222230122

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

## CODING 
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
dt=pd.read_csv("/content/titanic_dataset.csv")
dt

dt.info()

dt.shape

dt.set_index("PassengerId",inplace=True)
dt.describe()

dt.nunique()

dt["Survived"].value_counts()

per=(dt["Survived"].value_counts()/dt.shape[0]*100).round(2)
per


sns.countplot(data=dt,x="Survived")

dt

dt.Pclass.unique()

dt.rename(columns={'Sex':'Gender'},inplace=True)
dt

sns.catplot(x="Gender",col="Survived",kind="count",data=dt,height=5,aspect=.7)

sns.catplot(x="Survived",hue="Gender",data=dt,kind="count")

dt.boxplot(column="Age",by="Survived")

sns.scatterplot(x=dt["Age"],y=dt["Fare"])

sns.jointplot(x="Age",y="Fare",data=dt)


fig,ax1=plt.subplots(figsize=(8,5))
pt=sns.boxplot(ax=ax1,x="Pclass",y="Age",hue="Gender",data=dt)

sns.catplot(data=dt,col="Survived",x="Gender",hue="Pclass",kind="count")

corr=dt.corr()
sns.heatmap(corr,annot=True)

sns.pairplot(dt)
```


## OUTPUT

![Screenshot 2024-04-02 201659](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/f3144379-b9c3-4954-bd5e-64f1f7b8e5c3)

## INFO


![Screenshot 2024-04-02 201813](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/c8c3a1ed-a42f-4f9e-a92b-da6cc2db42f5)

## SHAPE


![Screenshot 2024-04-02 201854](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/af70e7da-89d1-4b53-81f9-cdff2ad76045)

## DESCRIBE

![Screenshot 2024-04-02 202041](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/f59240ae-0e22-4517-a780-a8da06e3c8b5)

## NUNIQUE

![Screenshot 2024-04-02 202945](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/9cf5065e-433a-4875-8b52-e4d38261a57b)

## VALUE COUNTS


![Screenshot 2024-04-02 203150](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/69fac243-6103-4e69-9217-8b6d12cf9fd5)

## VALUE COUNTS

![Screenshot 2024-04-02 203245](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/c299c270-aa39-41c3-9d86-3f1257ea4368)

## COUNTPLOT


![Screenshot 2024-04-02 203724](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/bd26ae04-387a-4a16-9f64-d4e061a05db5)

## DATA


![Screenshot 2024-04-02 203822](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/67102f26-3efe-41d3-8967-07bdd5b54011)

## PCLASS UNIQUE

![Screenshot 2024-04-02 203931](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/64cddbc8-79b9-40e3-9da2-7224e6b2dc8a)

## RENAME

![Screenshot 2024-04-02 204030](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/fa3e161f-c4ec-4e50-9bfb-1c27daa3c29b)

## CATPLOT

![Screenshot 2024-04-02 204145](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/25f50b13-08fc-42a2-9abc-879d85fa8b61)

## CATPLOT


![Screenshot 2024-04-02 204230](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/84e41259-0df9-40f1-8698-17a0df613a26)

## BOXPLOT


![Screenshot 2024-04-02 204324](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/d44664a8-06ed-4b35-bebf-278f852ad884)

## SCATTERPLOT


![Screenshot 2024-04-02 204410](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/f2d5c2cd-9edc-4c78-8d24-3ad14d191840)

## JOINTPLOT


![Screenshot 2024-04-02 204519](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/e71ded9a-5a6d-469d-8dd2-d3c1034da8dc)


## BOXPLOT

![Screenshot 2024-04-02 204637](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/b343d909-2cd6-4b52-93f8-eeb9050ff506)

## CATPLOT


![Screenshot 2024-04-02 204719](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/fe8dc6ea-faac-4eef-8f9a-44a73942359c)


## Co-relation


![Screenshot 2024-04-02 204839](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/a917a4ec-8923-4e6d-86fa-4d83231b2cb4)

## PAIR PLOT


![Screenshot 2024-04-02 205002](https://github.com/RENUGASARAVANAN/EXNO2DS/assets/119292258/914b657b-efa2-41f8-b36a-503515fcf999)


# RESULT
       Thus, the Exploratory Data Analysis on the given data set was performed successfully.
