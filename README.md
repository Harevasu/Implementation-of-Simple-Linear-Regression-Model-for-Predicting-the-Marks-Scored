# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard Libraries.
2. Set variables for assigning dataset values.
3. Import linear regression from sklearn.
4. Assign the points for representing in the graph.
5. Predict the regression for marks by using the representation of the graph.
6. Compare the graphs and hence we obtained the linear regression for the given datas. 

## Program:
### Developed by: Harevasu S
### RegisterNumber: 212223230069 
### Program to implement the simple linear regression model for predicting the marks scored.

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.metrics import mean_absolute_error,mean_squared_error
df=pd.read_csv("Untitled spreadsheet - Sheet1 (1).csv")
df.head()
df.tail()
X=df.iloc[:,:-1].values
X
Y=df.iloc[:,1].values
Y
from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test=train_test_split(X,Y,test_size=1/3,random_state=0)
from sklearn.linear_model import LinearRegression
regressor=LinearRegression()
regressor.fit(X_train,Y_train)
Y_pred=regressor.predict(X_test)
Y_pred
Y_test
plt.scatter(X_train,Y_train,color="red")
plt.plot(X_train,regressor.predict(X_train),color="blue")
plt.title("Hours vs Scores(Training Set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()
plt.scatter(X_test,Y_test,color='green')
plt.plot(X_train,regressor.predict(X_train),color='red')
plt.title("Hours vs Scores(Training Set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()
mse=mean_squared_error(Y_test,Y_pred)
print('MSE=',mse)
mae=mean_absolute_error(Y_test,Y_pred)
print('MAE=',mae)
rmse=np.sqrt(mse)
print('RMSE=',rmse)
```

## Output:
![1](https://github.com/user-attachments/assets/6f726895-d56a-4a17-a205-dbedec6b2bf1)

![2](https://github.com/user-attachments/assets/57d498d2-5088-4077-83f8-87886e935d00)


![3](https://github.com/user-attachments/assets/3582f145-d98d-423e-aa29-3d0d765dd033)

![4](https://github.com/user-attachments/assets/4caaad17-28a2-478d-bfda-4567c9281cbc)

![5](https://github.com/user-attachments/assets/8294b00a-9c28-47de-aa1c-b6b92d3ea1a8)

![6](https://github.com/user-attachments/assets/7c0b7fd6-d4e2-4d59-b31d-245c29f2cd15)



![image](https://github.com/user-attachments/assets/7843fea9-23bd-468d-a015-89aff85fff6d)

![image](https://github.com/user-attachments/assets/9b91ced8-bb5f-4821-ac93-9b7f5d1dc4da)



![9](https://github.com/user-attachments/assets/62d9c21c-bbe2-4bc6-8753-d39a0ea8db08)





## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
