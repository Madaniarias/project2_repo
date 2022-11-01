# QUIZ 018

## CODE
```.py
#QUIZ 18
#Create a function to help Lily

def numberMatches(lenght:int,speed:int)->int:
    matches = str(round((lenght/(speed/100))/5))
    return matches
#CASE 1
out = numberMatches(lenght=100,speed=100)
print(f"{out} matches")

#CASE 1
out = numberMatches(lenght=250,speed=110)
print(f"{out} matches")

#CASE 1
out = numberMatches(lenght=500,speed=150)
print(f"{out} matches")

#CASE 1
out = numberMatches(lenght=12345,speed=123)
print(f"{out} matches")
```
## TEST
![Screen Shot 2022-11-01 at 11 51 33](https://user-images.githubusercontent.com/111761417/199148204-e9d890d6-701e-4acd-9ef8-3cdfb7741636.png)

## TRUTH TABLE
![Untitled Notebook (26)-2](https://user-images.githubusercontent.com/111761417/199280509-cfc4ad1f-1acf-41d3-8f01-9aa88492fc4e.jpg)


