# QUIZ 020

## CODE
```.py
#a.Create a function that produces the table of truth for 3 inputs:
#table = get_truth()
#print(table)

def get_truth():
    print("| A | B | C |")
    A = False
    B = False
    C = False
    counter = 1
    for i in range(8):
        print (f"| {int(A)} | {int(B)} | {int(C)} |")
        if counter > 0 and counter % 4 == 0:
            A = not A
        if counter > 0 and counter % 2 == 0:
            B = not B
        C = not C
        counter += 1

table = get_truth()
print(table)
```
## TEST
![Screen Shot 2022-11-01 at 11 09 36](https://user-images.githubusercontent.com/111761417/199143318-281a831d-bd73-45fa-b405-11c00f7d6ac1.png)

## TRUTH TABLE AND CIRCUIT
![image](https://user-images.githubusercontent.com/111761417/200166581-2db31f39-fe8a-482f-92bb-34c7f8971760.png)

