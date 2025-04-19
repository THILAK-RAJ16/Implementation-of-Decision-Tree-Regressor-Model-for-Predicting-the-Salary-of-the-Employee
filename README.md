# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas

2. Import Decision tree classifier

3. Fit the data in the model

4. Find the accuracy score

## Program:

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
```
import pandas as pd
data=pd.read_csv(r"C:\Users\admin\Downloads\Salary.csv")

data.head()
data.info()
data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
print(data.head())

x=data[["Position","Level"]]
print(x.head())

y=data["Salary"]
y.head()

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
print(y_pred)

from sklearn import metrics
r2=metrics.r2_score(y_test,y_pred)
print(r2)

dt.predict([[5,6]])
```
Developed by: Thilak Raj . P

RegisterNumber:  212224040353


## Output:

![image](https://github.com/user-attachments/assets/96de3818-6f5f-4623-8bb2-71ad58abf05c)


![image](https://github.com/user-attachments/assets/d883f728-997a-424a-96a2-422664fa756d)

![image](https://github.com/user-attachments/assets/82590140-fad9-446f-8497-c0a26f82fecc)

![image](https://github.com/user-attachments/assets/97f4b4fd-380f-4287-ad98-f258fd16a963)

![image](https://github.com/user-attachments/assets/8b0093f4-f525-4101-af15-a3102a55e765)

![image](https://github.com/user-attachments/assets/c887f5ff-f0e1-46ea-a78e-97923fd11c7a)


![image](https://github.com/user-attachments/assets/45a59868-c367-4e8c-842f-72f288811ba5)

![image](https://github.com/user-attachments/assets/4d44abff-445e-400b-abc8-459a2cc8b8e7)

![image](https://github.com/user-attachments/assets/19840d2c-2d4a-441f-84d9-35aab0c06854)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
