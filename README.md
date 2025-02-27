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
	
![image](https://github.com/SivaramakrishnanBaskar/Univariate-Linear-Regression/assets/119476322/9ecf96f6-c0bd-4efa-bdc5-93085c39dc74)

4.	Compute the y -intercept of the line by using the formula:
	
![image](https://github.com/SivaramakrishnanBaskar/Univariate-Linear-Regression/assets/119476322/0bf542d5-b484-4081-a38b-d6a3957772b6)

5.	Use the slope m and the y -intercept to form the equation of the line.

6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program
```
Developed By: Sivaramakrishnan B
Register Number: 212222110044

import numpy as np
import matplotlib.pyplot as plt

x=np.array(eval(input()))
y=np.array(eval(input()))

xmean = np.mean(x)
ymean = np.mean(y)

num,den = 0,0
for i in range (len(x)):
    num += (x[i]-xmean)*(y[i]-ymean)
    den += (x[i]-xmean)**2
m = num/den
c = ymean-m*xmean 
print(m,c)

y_prad=m*x*c
print(y_prad)
plt.scatter(x,y)
plt.plot(x,y_prad,color="orange")
plt.show()
```

## Output:
![214855539-cd4badee-e254-4ebc-abd4-d61a455c4695](https://github.com/SivaramakrishnanBaskar/Univariate-Linear-Regression/assets/119476322/68e8f48e-f0db-423a-af90-3c8dfe560f8f)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
