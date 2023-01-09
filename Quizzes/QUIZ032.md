# QUIZ032

# CODE

```.py

#a. Compare the data from sensor 9 and 10 with smoothing of 12 samples
#b. What are the three main operators used in boolean logic?

import requests
from matplotlib import pyplot as plt
import numpy as np

req = requests.get('http://192.168.6.142/readings')
data = req.json()
readings = data['readings'][0]
print(len(readings))

#get only temperature
temp =[]
for sample in readings:
    if sample['sensor_id'] == 9:
        temp.append(sample['value'])

temp2 =[]
for sample in readings:
    if sample['sensor_id'] == 10:
        temp2.append(sample['value'])

number_samples_per_hour = 12
mean_per_hour = []
std_per_hour = []
x =[]
for t in range(0,len(temp), number_samples_per_hour):
    t_hour = temp[t:t+number_samples_per_hour] #12 values
    mean_per_hour.append(sum(t_hour)/len(t_hour))
    std_per_hour.append(np.std(t_hour))
    x.append(t)

mean_per_hour2 = []
std_per_hour2 = []
x2 = []
for t in range(0,len(temp2), number_samples_per_hour):
    t_hour = temp2[t:t+number_samples_per_hour] #12 values
    mean_per_hour2.append(sum(t_hour)/len(t_hour))
    std_per_hour2.append(np.std(t_hour))
    x2.append(t)

fig=plt.figure(figsize=(9,6))

plt.title("sensor #9")
plt.subplot(2,1,1)
plt.plot(x, mean_per_hour)

plt.title("sensor #10")
plt.subplot(2,1,2)
plt.plot(x, mean_per_hour2)
plt.show()

```

# TEST

![Screen Shot 2023-01-10 at 8 45 59](https://user-images.githubusercontent.com/111761417/211430465-f733d23f-053b-4e49-87f0-500c7a2f8846.png)


