
# **Example Programs**
## **1.Hello World Program**
Its a simple program  that describes how to input your name , age , designation and your three skills.You can workout this program as ice breaking one..
#### Source Code
```py
print("welcome to world of coding")
print("please fill the details")
name=input("enter your name -")
age=input("enter your age -")
designation=input("enter your designation -")
list=[]
for i in range(3):
    skills=input("please enter your skills:\n")
    list.append(skills)
print("my name is :",name)
print("my age is :",age)
print("I am ",designation)
print('i am mastered in ',*list,sep= "," )
```
#### Output
![output 1](https://user-images.githubusercontent.com/81223681/135761760-e09c79ac-3ee4-4cfd-996d-cc11811a12e6.png)

## **2.Multiplication Table Program**
Yeah! Ice breaked come on lets do an another program.This program is also a simple program but try it to ensure you are a good learner..
#### Source Code
```py
num=int(input("enter the nuber :"))
if (num%2)==0:
    print("{0} is even number".format(num))
    print ("multiplication table ")
    for i in range(1,11):
        print(num,'x',i,'=',num*i)
else:
    print("{0} is odd number".format(num))
    print ("multiplication table ")
    for i in range(1,11):
        print(num,'x',i,'=',num*i)
```
#### Output
![output 2](https://user-images.githubusercontent.com/81223681/135762192-93e5053f-7f5d-4ed0-8520-ef64da794403.png)

## **3.Pattern Printing Program**
Lets Go to next program , In the next program we will  print a simple pattern 
#### Source Code
```py
rows=int(input("Enter the number of rows :"))
for i in range(0, rows):
    for j in range(0, i + 1):
        print("#", end=' ')
    print("\r")

for i in range(rows, 0, -1):
    for j in range(0, i - 1):
        print("#", end=' ')
    print("\r")

```
#### Output
![output 3](https://user-images.githubusercontent.com/81223681/135836979-2cc3605e-ba5f-4b30-ad9d-35a669ccaa7f.png)

## **4.Calculator Program**
In this program we program a calculator that will do operations like

- 1.Addition
- 2.Substraction
- 3.Multiplication
-  3.Division
-  4.Square root of a number
- 5.Power of a Number

So lets go to the program..
#### Source Code
```py
print("Lets start calculating...")
def script():
    # define functions  
    def add(x, y):  
        return x + y 
    def subtract(x, y): 
        return x - y 
    def multiply(x, y):  
        return x * y 
    def divide(x, y): 
        return x / y 
    def percentage(x,y):
        return (x/y)*100
    def squart(x):
        return 
    def power(x,y):
        return
    print("Select operation.")  
    print("1.Add")  
    print("2.Subtract")  
    print("3.Multiply")  
    print("4.Divide")
    print("5.percentage")
    print("6.squareroot")
    print("7.power of n") 
  
    choice = input("Enter choice(1/2/3/4/5/6/7):")  
  
    num1 = int(input("Enter first number: "))  
    num2 = int(input("Enter second number: "))  
  
    if choice == '1':  
        print(num1,"+",num2,"=", add(num1,num2))  
    elif choice == '2':  
        print(num1,"-",num2,"=", subtract(num1,num2))  
  
    elif choice == '3':  
        print(num1,"*",num2,"=", multiply(num1,num2))  
    elif choice == '4':  
        print(num1,"/",num2,"=", divide(num1,num2))
    elif choice == '5':
        print("percentage=",percentage(num1,num2),"%")
    elif choice == '6':
        number = int(input("enter a number: "))
        sqrt = number ** 0.5
        print("square root:", sqrt)
    elif choice == '7':
        num = int(input("Enter the number of which you have to find power: "))
        pw = int(input("Enter the power: "))
        kj = 1
        for n in range(pw):
            kj = kj*num
        print(kj)
    else:  
        print("Invalid input") 
    restart =input("Would you like to continue ")
    if restart == "yes" or restart == "y":
            script()
    if restart == "n" or restart == "no":
            print ("Thank you for using me")
script()

```
#### Output
![output 4](https://user-images.githubusercontent.com/81223681/135838857-34cdcdde-44a1-4f8a-99c7-b000efe7c0e8.png)

## **5.Password Generator**
Lets Create a password Generator using Python . Compared to other programs this program is a difficult one .

#### Source Code
```py
print("DO YOU NEED PASSWORDS ? ")
print("I-N-O-S-A-F-E is here! lets make new passwords that improve your security. ")
def script():
    def restart():
        return 
    import random
    chars="abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ"
    chars1="abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890"
    chars2="abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890!@#$%^&*"
    print("Select password type.")  
    print("1.Standard")  
    print("2.Secure")  
    print("3.Ultra")
    choice = input("Enter your choice(1/2/3):")
    number=int(1)
    length=int(16)
    if choice == '1': 
        for p in range(number):
            password="INO_"
        for c in range(length):
                password += random.choice(chars)
        print(password)
    elif choice == '2':
        for p in range(number):
            password="INO_"
        for c in range(length):
                password += random.choice(chars1)
        print(password)
    elif choice == '3':
        for p in range(number):
            password="INO_"
        for c in range(length):
                password += random.choice(chars2)
        print(password)
    else:  
        print("Invalid input") 
    restart =input("Would you like to continue ")
    if restart == "yes" or restart == "y":            
             script()
    if restart == "n" or restart == "no":
            print ("Thank you for using me")
script()

```
#### Output
![output 5](https://user-images.githubusercontent.com/81223681/135841667-1e3a3a17-5e0e-4278-8a2e-e85e3d09a025.png)


## **6.Age Calculator**
We created a calculator  previously with all operations. But in this program we create a Age calculator in which use input his date of birth and user will get age in output. what are yow waiting lets do this..
#### Source Code
```py
from datetime import datetime, date
  
born=input("Enter your date of birth  in  the format(DD/MM/YYYY) :")
print("Your  date of birth is  ",born)
  
born = datetime.strptime(born, "%d/%m/%Y").date()
  
today = date.today()
print("Yeah It is true!")
print("You are",
      today.year - born.year - ((today.month,
                                          today.day) < (born.month,
                                                        born.day)),"years,",today.month - born.month -((today.year,
                                                                    today.day) < (born.year,born.day)),"month and",(today.day - born.day or born.day - today.day) -((today.month,
                                                                                     today.year) < (born.month,born.year)),"days old")

```
#### Output
![output 6](https://user-images.githubusercontent.com/81223681/135843146-bd0f7106-1d22-494d-90ca-8c25533f6686.png)


## **7.Guess the Number Game**
In this Example program we are going to create a Guess the number game Its logic is simple so lets check it out
#### Source Code
```py
import random

print("wekcome to guessing game ")
num = random.randint(1, 10)
guess = None

while guess != num:
    guess = input("guess a number between 1 and 10: ")
    guess = int(guess)

    if guess == num:
        print("congratulations! you won!")
        break
    else:
        print("nope, sorry. try again!")

```
#### Output
![output 7](https://user-images.githubusercontent.com/81223681/135884211-2e0d324b-ef32-4744-ab6d-07badf2dd4ea.png)

## **8.Weight Converter**
```py
weight = int(input("Enter your weight : "))
unit = input("Unit in which you entered the weight [(L)bs or (K)g ]: ")
if unit.upper() == "L":
    converted = weight*0.45
    print(f"You are {converted} kilograms")
else:
    converted = weight/0.45
    print(f"You are {converted} pounds")
```
## **Output**

![2021-10-05 (4)](https://user-images.githubusercontent.com/81372148/136081309-de3f2791-847f-404e-b8f0-b92f77a0cb91.png)
![2021-10-05 (5)](https://user-images.githubusercontent.com/81372148/136080831-8e843295-de43-451e-9743-a6270671cb59.png)
   
