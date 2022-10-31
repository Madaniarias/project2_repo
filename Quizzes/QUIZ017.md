# QUIZ 017

## CODE

```.py
#Creating function with name averageLength
def averageLength(words:int)->int:
    return sum([len(i.strip()) for i in words])/len(words)

#CASE 1
out = averageLength(words = ["hello","main"])
print(out)
#CASE 2
out = averageLength(words = ["Peru","France","Nepal"])
print(out)
#CASE 3
out = averageLength(words = ["Computer Science","Art"])
print(out)
#CASE 4
out = averageLength(words = ["one", "two"])
print(out)
```
## TEST
![Screen Shot 2022-10-31 at 21 27 01](https://user-images.githubusercontent.com/111761417/199007632-d605939a-7499-4171-bff1-c665add5328c.png)
## FLOW DIAGRAM
