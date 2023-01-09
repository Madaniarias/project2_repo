# QUIZ028

# CODE

```.py
#a. Create a graph for the x,y data below:
from matplotlib import pyplot as plt
data ={
    "x": [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19] ,
    "y": [24,1,2,25,26,21,23,34,49,2,19,32,7,17,36,7,45,28,40,46] ,
    "title" : "quiz028"}

#Add a the item "title:"quiz028" to the dictionary

plt.plot(data['x'],data['y'], color="b", marker="o")
plt.xlabel("x")
plt.ylabel("y")
plt.title(data['title'])
plt.show()
```

# TEST

![Screen Shot 2023-01-10 at 0 35 33](https://user-images.githubusercontent.com/111761417/211346486-508f46f5-b6ad-4cab-9883-f50741d216c8.png)

# RGB TO HEX

![image](https://user-images.githubusercontent.com/111761417/211347625-ec9ab238-957e-44b1-a0ef-9ca739498e86.png)

