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
![Screen Shot 2022-11-15 at 9 40 17](https://user-images.githubusercontent.com/111761417/201798065-c167c342-01af-463e-a8a3-b23b416aa0ff.png)

## CONVERT TO DECIMAL

To convert FFA5 (hexadecimal system) to decimal we have:
F : 15
F : 15
A : 10
5 : 5

Then, we multiply each number value by 16 (hexadecimal base) raised to the position of each value from right lo left:
F : 15 * 16^3 = 61440
F : 15 * 16^2 = 3840
A : 10 * 16^1 = 160
5 : 5 * 16^0 = 5 

Lastly, we sum all the numbers up and we will obtain the decimal equivalent of "FFA5":
61440 + 3840 + 160 + 5 = 65445
