# QUIZ024

# CODE
```.py

import random
random.seed(1234)
x_out = []
y_out = []
st = -10
for i in range (100):
    x_out.append(st)
    y = 2*(st+5)**2
    y_out.append(y)
    y_str = f"{y:2f}"
    st +=0.2

from matplotlib import pyplot as plt

plt.plot(x_out,y_out, color="g", marker="o")
plt.xlabel("x")
plt.ylabel("2(x+5)**2")
plt.show()
```
# TEST
![Screen Shot 2022-11-12 at 14 23 39](https://user-images.githubusercontent.com/111761417/201458752-4ad8f8f8-72dc-4ba0-88df-1ed080a984cc.png)

# CIRCUIT
![image](https://user-images.githubusercontent.com/111761417/201461659-447ae923-a032-4820-982f-f461e967145b.png)

