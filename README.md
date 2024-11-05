# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required library and read the dataframe.

2.Write a function computeCost to generate the cost function.

3.Perform iterations og gradient steps with learning rate.

4.Plot the Cost function using Gradient Descent and generate the required graph. 

## Program:

```

/*
Program to implement the linear regression using gradient descent.
Developed by: DHARSHAN D
RegisterNumber: 212223230045

import numpy as  np
import pandas as pd
from sklearn.preprocessing import StandardScaler
def linear_regression(x1,y,learning_rate=0.01,num_iters=100):
  X=np.c_[np.ones(len(X1)),x1]
  theta=np.zeros(X.shape[1]).reshape(-1,1)

  for _ in range(num_iters):
    predictions=(X).dot(theta).reshape(-1,1)
    errors=(predictions-y).reshape(-1,1)        
    theta=learning=learning_rate*(1/len(X1))*X.T.dot(errors)
  return theta

data=pd.read_csv("50_Startups.csv")
print(data.head())
X=(data.iloc[1:,:-2].values)
print(X)
X1=X.astype(float)
scaler=StandardScaler()
y=(data.iloc[1:,-1].values).reshape(-1,1)
print(y)
X1_Scaled=scaler.fit_transform(X1)
Y1_Scaled=scaler.fit_transform(y)
print(X1_Scaled)
print(Y1_Scaled)
theta=linear_regression(X1_Scaled,Y1_Scaled);

new_data=np.array([165349.2,136897.8,471784.1]).reshape(-1,1)
new_Scaled=scaler.fit_transform(new_data)
prediction=np.dot(np.append(1,new_Scaled),theta)
prediction=prediction.reshape(-1,1)
pre=scaler.inverse_transform(prediction)
print(f"Predicted value: {pre}")
*/
```

## Output:
DATA.HEAD()

![Screenshot 2024-08-29 183415](https://github.com/user-attachments/assets/763022ca-616b-4141-942a-109ee33e0446)

X VALUE 

![image](https://github.com/user-attachments/assets/83d89cce-8fa6-491b-9c3f-6c18f2c63c3c)

X1_SCALED VALUE 

![image](https://github.com/user-attachments/assets/0920d359-e997-46a2-844c-740ef89f149a)

PREDICTED VALUES:

![image](https://github.com/user-attachments/assets/eb585b7f-3b99-40c0-ab3a-9c6072a7ed39)

## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
