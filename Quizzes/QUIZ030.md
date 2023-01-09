# QUIZ030

# CODE

```.py 

#a. Using the data in the learning log (item 21), create a graph with a smoothed version where the smoothing window is every 4 points.
#[HL] Smoothing window overlaps 50%
import numpy as np
from matplotlib import pyplot as plt
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
number_samples_per_hour = 4
mean_per_hour = []
std_per_hour = []
x =[]
for t in range(0,len(h), number_samples_per_hour//2):
    t_hour = h[t:t+number_samples_per_hour] #12 values
    mean_per_hour.append(sum(t_hour)/len(t_hour))
    std_per_hour.append(np.std(t_hour))
    x.append(t)

fig=plt.figure(figsize=(9,6))
plt.subplot(2,1,1)
plt.plot(h)
plt.subplot(2,1,2)
plt.plot(x, mean_per_hour)
plt.show()

```

# TEST

![Screen Shot 2023-01-10 at 0 50 50](https://user-images.githubusercontent.com/111761417/211349938-496b25c8-b5d3-46c7-b987-d9ab250bea88.png)


# QUESTION
a. When was the internet first created? Remember to add your sources.



