# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import the standard libraries. 2.Upload the dataset and check for any null values using .isnull() function. 3.Import LabelEncoder and encode the dataset. 4.Import DecisionTreeClassifier from sklearn and apply the model on the dataset. 5.Predict the values of array. 6.Import metrics from sklearn and calculate the accuracy of the model on the dataset. 7.Predict the values of array. 8.Apply to new unknown values.

## Program:
```
/*

Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: PAVAN KISHORE.M
RegisterNumber:  212221230076

import pandas as pd
data=pd.read_csv("Employee.csv")
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
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:
## DATA HEAD
![TTT1](https://user-images.githubusercontent.com/94154941/173227566-05eac30b-5bbb-4074-8ec0-97354ca22991.png)
## DATA INFO
![TTT2](https://user-images.githubusercontent.com/94154941/173227602-8cdd5cdb-7371-41a9-a450-4e58aa6cac26.png)

## DATA ISNULL
![TTT3](https://user-images.githubusercontent.com/94154941/173227596-64f9284c-fb2c-4410-b4aa-c7d0f0e60548.png)


## DATA LEFT
![TTT4](https://user-images.githubusercontent.com/94154941/173227594-6af0baf6-4d92-491f-bdc1-2a61d6fa70bb.png)


## X HEAD
![TTT5](https://user-images.githubusercontent.com/94154941/173227591-009dc134-a8d2-48bd-89f8-985138175bc2.png)

## DATA FIT
![TTT6](https://user-images.githubusercontent.com/94154941/173227587-abead1eb-c584-4610-8b68-c17850cb5ea6.png)


## ACCURACY
![TTT7](https://user-images.githubusercontent.com/94154941/173227584-84ec729a-16ab-4e2a-9750-dccc1a843ca7.png)


## PREDICTED VALUES
![TTT8](https://user-images.githubusercontent.com/94154941/173227580-abd3a82d-b9fe-41a6-af3b-7216fc4299c4.png)


Result:
Thus the program to implement the Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
