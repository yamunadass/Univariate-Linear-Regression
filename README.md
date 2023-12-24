# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
The program was developed by:Yamuna M
Register Number:212223230248

import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
xmean = np.mean(x)
ymean = np.mean(y)
num, den = 0,0
for i in range (len(x)):
  num += (x[i] - xmean)*(y[i] - ymean)
  den += (x[i] - xmean)**2
m=num/den
c=ymean - (m*xmean)
print(m,c)
y_pred = m*x+c
print(y_pred)
plt.scatter(x,y)
plt.plot(x,y_pred, color = "orange")
plt.show()
```
## Output
![image](https://github.com/yamunadass/Univariate-Linear-Regression/assets/138971172/d15719a7-48bf-402e-a873-0ccbd2234097)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
