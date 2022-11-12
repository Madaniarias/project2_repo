# QUIZ 021

## CODE
```.py
#Unisng the function that produces the table of Truth for 3 inputs, add a column for the boolean equation
#AB + (not B) + (notB C)
def get_truth():
    print("| A | B | C | AB + (not B) + (notB C) |")
    A = False
    B = False
    C = False
    D = A and B or (not B) or (not B and C)
    counter = 1
    for i in range(8):
        print (f"| {int(A)} | {int(B)} | {int(C)} | {int(D)}")
        if counter > 0 and counter % 4 == 0:
            A = not A
        if counter > 0 and counter % 2 == 0:
            B = not B
        C = not C
        D = A and B or (not B) or (not B and C)
        counter += 1

table = get_truth()
print(table)
```
## TEST
![Screen Shot 2022-11-11 at 1 13 11](https://user-images.githubusercontent.com/111761417/201148330-d1ea7f72-6d3f-4ac7-9200-a3923906b6b2.png)

## TRUTH TABLE AND CIRCUIT
![image](https://user-images.githubusercontent.com/111761417/201460880-88bf03f6-50dc-4c83-a293-49610bd40bb4.png)
