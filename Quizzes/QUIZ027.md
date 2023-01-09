# QUIZ027

# CODE

```.py
#Create a errorbar graph fpr the data below. You will need to calculate the mean and standard deviation first.
from matplotlib import pyplot as plt
import numpy as np
plt.style.use("dark_background")

sensorA = [16,24,24,9,23,26,26,23,25,14]
sensorB = [2,19,25,10,11,24,17,7,24,17]
sensorC = [15,11,24,21,6,2,18,27,1,16]

#Step 1: Visualize data
samples = [] # empty list
for i in range(len(sensorA)):
    samples.append(i)

fig = plt.figure(figsize=(8,4))

#Step 3: Analyxe the data
mean=[]
standard_dev=[]
for i in range (len(sensorA)):
    data = [sensorA[i], sensorB[i],sensorC[i]]
    mean.append(np.mean(data))
    standard_dev.append(np.std(data))

plt.title("Sensors")
plt.ylabel("Y")
plt.xlabel("X")
plt.fill_between(samples,sensorA,sensorB,sensorC, alpha=.5,linewidth=0,color="#8ecae6")
plt.errorbar(samples, mean, standard_dev, fmt="*")
plt.show()

```

# TEST

![Screen Shot 2023-01-10 at 0 21 15](https://user-images.githubusercontent.com/111761417/211343272-3f8080fb-d278-450d-ace4-e2ea7ee8b277.png)

# RGB TO HEX

![image](https://user-images.githubusercontent.com/111761417/211345809-c70ed6a7-7dc7-4c6f-987f-e604edbda821.png)
