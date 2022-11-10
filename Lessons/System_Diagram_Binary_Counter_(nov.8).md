# System Diagram Binary Counter (Nov. 8)

![Screen Shot 2022-11-11 at 1 28 47](https://user-images.githubusercontent.com/111761417/201152092-4c8e53ac-fe91-420e-a81f-4f9dc6ba4a59.png)

# Materials

The materials used for the activity were:
- 3 LED lights
- MacBook Air Laptop
- 1 USB cable
- 1 breadboard
- 1 Arduino
- 3 resisors
- 7 cables 

# BUILDING THE HARDWARE 

![image](https://user-images.githubusercontent.com/111761417/201153192-b2dddf98-c706-4c41-9833-6200f271aa3d.png)
<sub> Fig 1. Hardware for the binary counter. 
  
# CODE
  
```.py
#Importing pyfrimata from Ardino
from pyfirmata import Arduino
import time

if __name__ == '__main__':
    board = Arduino('/dev/cu.usbserial-1420')
    print("communication successfully started")
    
  #Establishing variable names 
  # 1 = ligth on / 0 = light off
    a=1
    b=1
    c=1
    
    while True:
        for i in range(0, 8, 1):    
            if i % 4 == 0:
                a = not a
            if i % 2 == 0:
                b = not b
            c = i%2
            board.digital[5].write(int(a))
            board.digital[9].write(int(b))
            board.digital[12].write(int(c))
            time.sleep(1)
```

# TEST

Video_binary_counter_(nov.8)
  
  
