# Linear-regression
import pandas as pd 
d1=pd.read_csv('Salary_Data.csv')
#print(d)
import numpy as np
y = d1['YearsExperience']
x=d1['Salary']
summation = 0  
n = len(y)
#for i in range(0,1000):
yp=[]
def mse(b0,b1):
  for i in range (0,n):
    y_bar =(b1*x[i])+b0
    dif =(y[i]-y_bar)**2 
    yp.append(dif)
  ypp=np.array(yp)
  MSE = np.mean(ypp)
  print("The Mean Square Error for b0=",b0,"b1=", b1,"is: ",MSE)
for i in range(0,100):
      mse(i,i+1)
