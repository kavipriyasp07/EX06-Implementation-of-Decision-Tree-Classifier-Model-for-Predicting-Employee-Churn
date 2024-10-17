# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the Dataset: Use pandas to load the dataset (CSV, Excel, etc.) into a DataFrame.
2. Handle Missing Values: Identify and fill or drop missing values.
3. Encode Categorical Variables: Use label encoding or one-hot encoding for categorical data
(e.g., department, gender).
4. Split the Dataset: Divide the dataset into features (X) and target (y), then split into training and
testing sets.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:kavipriya S.P 
RegisterNumber: 2305002011
*/
import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv('/content/Employee_EX6.csv')
data=df.copy()
data.describe()
le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data
X=data.drop(['Departments','left'],axis=1)
Y=data['left']
clt=DecisionTreeClassifier()
clt.fit(X,Y)
plt.figure(figsize=(80,80))
plot_tree(clt,feature_names=X.columns,class_names=['LEFT','NOT LEFT'],filled=True)
plt.show()
```

## Output:
![Screenshot 2024-10-17 112139](https://github.com/user-attachments/assets/0cb20de5-63b2-49c8-8bd1-ac94b986ca6a)

![Screenshot 2024-10-17 112205](https://github.com/user-attachments/assets/28968c42-6265-45e4-89dc-c933b7b22dfe)
![Screenshot 2024-10-17 112221](https://github.com/user-attachments/assets/a8b5c99b-caa9-4876-9ba8-35acc58542c2)

![Screenshot 2024-10-17 111635](https://github.com/user-attachments/assets/143449e0-c431-4da5-957c-934ad600ec3b)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
