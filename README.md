# SURVIVAL-OF-TITANIC
#PPS MINI PROJECT
#Load the required libraries
import pandas as pd
import numpy as np
import seaborn as sns

#Load the data
df = pd.read_csv('titanic.csv')


#View the data
df.head()
#Basic information

df.info()

#Describe the data

df.describe()
#Find the duplicates

df.duplicated().sum()
#unique values

df['Pclass'].unique()

df['Survived'].unique()

df['Sex'].unique()
array([3, 1, 2], dtype=int64)


array([0, 1], dtype=int64)


array(['male', 'female'], dtype=object)
#Plot the unique values

sns.countplot(df['Pclass']).unique()
#Find null values

df.isnull().sum()
#Replace null values

df.replace(np.nan,'0',inplace = True)

#Check the changes now
df.isnull().sum()
#Datatypes

df.dtypes
#Filter data

df[df['Pclass']==1].head()
#Boxplot

df[['Fare']].boxplot()
#Correlation 

df.corr()
#Correlation plot

sns.heatmap(df.corr())
