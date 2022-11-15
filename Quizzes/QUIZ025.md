# QUIZ025

## CODE
```.py
#Create a program that shows the graph of the function below for 100 valuesof x in the interval -10 < x < 10

import random
random.seed(1234)
x_out = []
y_out = []
st = -10
for i in range (100):
    x_out.append(st)
    y = abs(st)
    y_out.append(y)
    y_str = f"{y:2f}"
    st +=0.2

from matplotlib import pyplot as plt

plt.plot(x_out,y_out, color="b", marker="o")
plt.xlabel("x")
plt.ylabel("f(x)=|x|")
plt.show()
```
## TEST


## CONVERT TO DECIMAL
