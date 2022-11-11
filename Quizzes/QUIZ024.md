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


# CIRCUIT
