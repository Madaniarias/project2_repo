# QUIZ029

# CODE 

```.py 
#a. Create a function that receives a dictionary with letters in the alphabet
#as keys and a string.
#The functions returns the dictionary with a count as a value for the
#ocurrence of each letter:



def count_letters(my_dict:dict, msg:str)->dict:
    for letter in msg:
        if letter in my_dict.keys():
            my_dict[letter]+=1
    return my_dict

case1 = count_letters(my_dict={'w':0, 'l':0, 'c':0}, msg="hello world")
print(case1)

case2 = count_letters(my_dict={'a':0, 'e':0, 'i':0, 'o':0, 'u':0}, msg="Why did I choose CS?")
print(case2)

```

# TEST

![Screen Shot 2023-01-10 at 0 46 39](https://user-images.githubusercontent.com/111761417/211348978-99486535-f162-410a-ac75-ad8e8debc255.png)

# QUESTION
a. How many different colors could you represent in a 6 bit computer? 
64 colors
because 2^6 = 64.

