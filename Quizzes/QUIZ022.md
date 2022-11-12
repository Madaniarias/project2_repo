# QUIZ 022

## CODE
```.py
#Create a program that produces n random values from the equation below, where m and s are the oter inputs of the function.
import random

random.seed(1234)
def produce (n:int, m:int, s:int):
    print(f"|{'x'.center(10)}|{'y(x)'.center(10)}|")
    x_out = []
    y_out = []
    for _ in range(n):
        x = random.randint(0,100)
        x_out.append(x)
        y = x ** (1/2*((m/s)**2))
        y_out.append(y)
        y_str = f"{y:.2f}"
        answer = print(f"|{str(x).center(10)}|{y_str.center(10)}|")

    return answer

sample = produce(n=5, m=3, s=2)
print(sample)
```
## TEST
![Screen Shot 2022-11-11 at 0 58 21](https://user-images.githubusercontent.com/111761417/201143966-ea7a5da9-b69c-4608-84b6-ace3252b496b.png)

## PROOF THAT...
![image](https://user-images.githubusercontent.com/111761417/201145976-426539e5-fe1f-458a-8ee1-01603fbc7bf6.png)
