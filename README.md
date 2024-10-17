# EX 5 Implementation of Logistic Regression Using Gradient Descent

## AIM:
To write a program to implement the the Logistic Regression Using Gradient Descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.<p>
2.Upload and read the dataset.<p>
3.Check for any null values using the isnull() function.<p>
4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.

## Program:
```
/*
Program to implement the the Logistic Regression Using Gradient Descent.
Developed by: K.Nishal
RegisterNumber:  2305001021
*/
import pandas as pd
import numpy as np
data=pd.read_csv("/content/ex45Placement_Data.csv")
data.head()
data1=data.copy()
data1.head()
data1=data1.drop(['sl_no','salary'],axis=1)
data1
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"])
data1["status"]=le.fit_transform(data1["status"])
data1
X=data1.iloc[:,:-1]
Y=data1["status"]
y_pred=predict(theta,X)
accuracy=np.mean(y_pred.flatten()==y)
print("Accuracy:",accuracy)
print("Predicted:\n",y_pred)
print("Actual:\n",y.values)
xnew=np.array([[0,87,0,95,0,2,78,2,0,0,1,0]])
y_prednew=predict(theta,xnew)
print("Predicted Result:",y_prednew)
```

## Output:
![WhatsApp Image 2024-10-04 at 21 13 12_d29c6482](https://github.com/user-attachments/assets/5e2e7109-79cd-4999-9ad1-7dc75502a0a2)
![WhatsApp Image 2024-10-04 at 21 13 45_fe7b599f](https://github.com/user-attachments/assets/ce2df77e-a1f4-46ac-91cd-0e181cbf73b4)



## Result:
Thus the program to implement the the Logistic Regression Using Gradient Descent is written and verified using python programming.

