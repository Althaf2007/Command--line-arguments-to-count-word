# Command--line-arguments-to-count-word
## AIM:
To write a python program for getting the word count from the contents of a file using command line arguments.
## EQUIPEMENT'S REQUIRED: 
PC
Anaconda - Python 3.7
## ALGORITHM
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## PROGRAM
```
import numpy as np
import matplotlib.pyplot as plt

x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)
plt.show()

xmean = np.mean(x)
ymean = np.mean(y)

num = 0
den = 0

for i in range(len(x)):
    num += (x[i]-xmean)*(y[i]-ymean)
    den += (x[i]-xmean)**2

m = num/den
b = ymean-m*xmean
print(m,b)

ypred = m*x + b
print(ypred)

plt.scatter(x,y,color='red')
plt.plot(x,ypred, color='blue')
plt.show()


```
### OUTPUT:
![439612296-07244e05-6b5f-4ec2-8cb4-94620dccd3e7](https://github.com/user-attachments/assets/7a3ca907-264c-49ee-9030-685eb2822fb7)
![439612348-0c0e4027-61e3-49a5-b6a6-850b24043575](https://github.com/user-attachments/assets/287f0814-f861-4329-abe6-305a1fa115d0)

## RESULT:
Thus the program is written to find the word count from the contents of a file using command line arguments.
