# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas module and import the required data set.
2.Find the null values and count them.

3.Count number of left values.

4.From sklearn import LabelEncoder to convert string values to numerical values.

5.From sklearn.model_selection import train_test_split.

6.Assign the train dataset and test dataset.

7.From sklearn.tree import DecisionTreeClassifier.

8.Use criteria as entropy.

9.From sklearn import metrics. 10.Find the accuracy of our model and predict the require values.
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:MONISH R 
RegisterNumber:212223220061

import pandas as pd
data=pd.read_csv("/content/Employee.csv")

data.head()

data.info()

data.isnull().sum()

data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["salary"]=le.fit_transform(data["salary"])
data.head()


x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()

y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
accuracy= metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:
## data.head():
![275247715-fdbb3b50-c6eb-44ce-9594-5f2c7d628cd1](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/154746066/dde1f14e-8426-4c96-b6c0-20e55c793ab1)

## data.info():
![275247763-73114c42-c06c-4482-8eb4-0fab603a3b5c](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/154746066/e77f565f-ef7e-42ed-9609-4e231427739e)

## isnull() and sum():
![275247815-769340ec-1d62-4772-8620-1d4b900b7193](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/154746066/72e9488b-d7c1-40f3-aacd-6907fd8545ee)

## data value counts():
![275247850-4d52e057-ebd2-4c86-bddc-b0a0744dc5d3](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/154746066/a8feebd2-2fba-44a0-9ba9-b9075f0ba5dd)

## data head() for salary:
![275247861-176d00f5-356f-472d-867f-511492b37082](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/154746066/e1eb23d7-c1e7-443a-ac22-3edf27a9fdc4)

# x.head():
![275247864-5743beab-0398-4f43-98a7-cb7b7b6b8e6e](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/154746066/c28faff3-c90e-446c-9415-5f3dc23a5423)

# accuracy value:
![275247980-9f1035e5-cef1-4f83-a9cd-d22773b47dc1](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/154746066/151a672f-e07a-4407-8a3a-a1fe19df409e)

# data prediction:
![275247872-535baeb1-6238-4e53-82a0-a2618d3d5aed](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/154746066/f0618d54-72e6-4138-a882-ff465c75f114)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
