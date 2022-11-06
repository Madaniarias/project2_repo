# QUIZ 019

## CODE
```.py
#Create a function that changes the vowels in a string to numbers such as a=4, e=3, i=1, o=0 and space by _
#case1 = get_l3tt3r(msg = "Hello World")
#print(case1)

def get_l3tt3r(msg:str)->str:
    character_changes = {"a": "4", "e": "3", "i": "1", "o": "0", " ": "_"}
    out = ""
    for i in msg:
        if i in character_changes:
            out = out + character_changes[i]
        else:
            out = out + i

    return out

#CASE 1
case1 = get_l3tt3r(msg="Hello World")
print(case1)
#CASE 2
case2 = get_l3tt3r(msg="Why did I choose CS?")
print(case2)
#CASE 3
case3 = get_l3tt3r(msg="Remember the Figure Caption")
print(case3)
```
## TEST
![Screen Shot 2022-11-01 at 23 46 19](https://user-images.githubusercontent.com/111761417/199261743-3d095010-f462-45dd-a9e8-cfd4179cfed3.png)

## CIRCUIT
![Untitled Notebook (26)-1](https://user-images.githubusercontent.com/111761417/199280225-3e70fc81-5be3-463e-bb73-a52596c9e1c7.jpg)

