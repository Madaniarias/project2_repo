# QUIZ031

# CODE

```.py
#Connect to the server and download the recordingd data. From the data, build a linear model between t=610 and t=800
#[HL] use a quadratic model y = ax2 + bx + c

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
    if sample['sensor_id']==1:
        temp.append(sample['value'])
#slice temperature to teh region of interest
temp_afternoon_mon=temp[610:800]
x_afternoon_mon = []
for i in range(len(temp_afternoon_mon)):
    x_afternoon_mon.append(i)

plt.scatter(x_afternoon_mon, temp_afternoon_mon)
#linear model
m,b=np.polyfit(x_afternoon_mon,temp_afternoon_mon,1)
x_line = [0,len(temp_afternoon_mon)]
y_line = []
for i in x_line:
    y_line.append(m*i*b)

plt.plot(x_line, y_line, 'black')

#quadratic model
a1,a2,a3 =np.polyfit(x_afternoon_mon, temp_afternoon_mon,2)
y_model_quad =[]
for i in x_afternoon_mon:
    y_model_quad.append(a1*(i)**2 + a2*i + a3)

plt.plot(x_afternoon_mon, y_model_quad)
plt.show()

```
# TEST
![Screen Shot 2023-01-10 at 8 40 23](https://user-images.githubusercontent.com/111761417/211429900-17375ded-7dde-4517-8830-30e0d3ee0eb2.png)

