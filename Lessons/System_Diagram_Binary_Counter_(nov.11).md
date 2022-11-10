# System Diagram Binary Counter (Nov. 11)

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

![Image_20221110_23215_239 PM](https://user-images.githubusercontent.com/111761417/201157541-2ba251de-2572-4946-ac7a-9d17f414610d.jpeg)


<sub> Fig 1. Hardware for the binary counter. 
  
# CODE
  
```.py
from pyfirmata import Arduino
import time

val = 0

def validate_int_between(msg, startNum, endNum):
    while True:
        try:
            val = int(input(f"{msg}: "))
            if val >= startNum and val <= endNum:
                return val
            else:
                print(f"Please enter a number between 0 and 7")
        except ValueError:
            print(f"Please enter an integer")

if __name__ == '__main__':

    board = Arduino('/dev/cu.usbserial-1420')
    print("communication successfully started")
    
    a=1
    b=1
    c=1
    
    while True:
        num = validate_int_between("Please enter a number between 0 and 7", 0, 7)
        
        for i in range(0,8,1):
            if i % 4 == 0:
                a = not a
            if i % 2 == 0:
                b = not b
            c = i%2

            if i == num:
                print(f"Number: {i}, binary: {int(a),int(b),int(c)}")
                board.digital[5].write(int(a))
                board.digital[9].write(int(b))
                board.digital[12].write(int(c))
                time.sleep(1)
```

# TEST

[Video_binary_counter_(nov.8)
](https://github.com/Madaniarias/unit2_repo/blob/main/Lessons/VIDEO%20binary%20counter%20nov.8.mp4)  
  
