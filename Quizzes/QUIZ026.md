# QUIZ026

# CODE

```
#26. Create a program that ① show the graph and ②create a linear (H_model = m*h+b) for the data below:
#h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]  
#Where h is relative humidity (%)

import matplotlib.pyplot as plt
import numpy as np
plt.style.use("dark_background")

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
samples = []
for i in range(len(h)):
    samples.append(i)

m,b = np.polyfit(samples,h,1)
x = []
y = []
for i in [0,30]:
    x.append(i)
    temp = m * i + b
    y.append(temp)

plt.plot(samples, h, linestyle="none", marker="+")
plt.ylabel("relative Humidity (%)")
plt.xlabel("samples")
plt.title("Graph of Relative Humidity")
plt.plot(x,y)
plt.show()

```.py 

# TEST

![Screen Shot 2023-01-10 at 0 09 22](https://user-images.githubusercontent.com/111761417/211342120-513fda34-7ef6-4d71-84fe-a3a39e896eed.png)

# HEX TO RGB

Convert the following color in hex to rgb:
#e6e627

![image](https://user-images.githubusercontent.com/111761417/211342065-2b0be72f-d145-4881-a66e-535c6ac102ed.png)





