# PLOTTING GRAPHS

# CODE
```.py
import matplotlib.pyplot as plt
import numpy as np

x = [1,2,3,1.5,4,2.5,6,4,3,5.5,5,2]
y = [3,4,8,4.5,10,5,15,9,5,16,13,3]

plt.scatter(x,y)
plt.title("Scatter Plot title")
plt.xlabel("X")
plt.ylabel("Y")

#Plot the equation y = mx + b 1 < x <7
m, b = np.polyfit(x, y, 1)
print(f"Linear equation is y={m:.2f}x+({b:.2f})")
model_x = []
model_y = []
for i in [1,6]:
    model_x.append(i)
    model_y.append(m*i+b)
plt.plot(model_x,model_y)
plt.show()
```

## NOTES
"curve fitting"
- calculation distance form point to line, sum of al distances making it as small as posible (find the line that makes the smallest d).
- order = power
    model is y =mx + b 
    where m and b are the parameters.

## HOMEWORK

Graph making in python
key words: linear recreation, function graphing, best fit, how to use matplotlib
