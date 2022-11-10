# QUIZ023

# CODE
```.py
#Create a program that produces the graph for the function in Quiz #22  
import random

random.seed(1234)
def produce(n:int, m:int, s:int):
    print(f"|{'x'.center(10)}|{'y(x)'.center(10)}|")
    x_out = []
    y_out = []
    for _ in range(n):
        x = random.randint(0, 100)
        x_out.append(x)
        y = x ** (1/2*((m/s)**2))
        y_out.append(y)
        y_str = f"{y:2f}"
      
    return y_out, x_out

data_y, data_x = produce(n=10, m=5, s=2)
from matplotlib import pyplot as plt

plt.plot(data_x, data_y, color="b", marker="o")
plt.xlabel("x")
plt.ylabel("x ** (1/2*((m/s)**2))")
plt.show()
```
# TEST
![Screen Shot 2022-11-11 at 1 21 16](https://user-images.githubusercontent.com/111761417/201150199-a91217c2-9d05-430c-a01e-0fd28952921e.png)

# TRUTH TABLE

