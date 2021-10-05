# Python Programming Language

## 💻 Introduction

[Python](https://www.python.org/) is an interpreted **high-level general-purpose programming language**. Its design philosophy emphasizes code readability with its use of significant indentation. Its language constructs as well as its object-oriented approach aim to help programmers write clear, logical code for small and large-scale projects.

## 💻 How to install & Configure

[![image](https://user-images.githubusercontent.com/44474792/123229167-ac6e8e00-d4f3-11eb-997b-a7149c967010.jpg)](https://youtu.be/AKVRkB0fot0)

## 💻 Resource Links to get started

### ⭐️ HackerRank

**[HackerRank](https://www.hackerrank.com/domains/python)** is a place where programmers from all over the world come together to solve problems in a wide range of Computer Science domains such as **Algorithms, Machine Learning, or Artificial Intelligence,** as well as to learn & practice different programming languages like **Python, JavaScript, C, C++, Java, Ruby** & much more...

[![image](https://user-images.githubusercontent.com/44474792/123522719-bd2e2800-d6dc-11eb-9175-3c9c62e44f9c.jpg)](https://www.hackerrank.com/domains/python)

### ⭐️ Scrimba

**[Scrimba](https://scrimba.com/)** is the next-generation platform for learning how to code. It is an interactive learning platform for mainly frontend developers. But they recently started adding courses for the backend as well. The screencasts enable learners to interact with the code directly in the player. The content on Scrimba is a mix between community generated tutorials, and courses initiated by the Scrimba team itself.

Some of them are:

- 🔰 [Python Basics](https://scrimba.com/playlist/peaXwtB) (9 Interactive Screencasts)
- 🔰 [Python | Introduction to Programming](https://scrimba.com/playlist/p5gW5AD) (21 Interactive Screencasts)
- 🔰 [Learn Python for free](https://scrimba.com/learn/python) (59 Interactive Screencasts)

[![image](https://user-images.githubusercontent.com/44474792/123522683-7809f600-d6dc-11eb-852f-184cb0f16421.jpg)](https://scrimba.com/learn/python)

### ⭐️ Programiz

**[Programiz](https://www.programiz.com/python-programming)** provides a beginner-friendly mobile app. It contains byte-size lessons and an integrated Python interpreter. **Learn Python: Programiz** is a free app that makes it easy to learn Python and try out what you have learned in real-time. If the platform suites, one can go for a subscription **Learn Python: Programiz Pro**, that offers challenges ans certification.

- 🔰 [Web Platform](https://www.programiz.com/python-programming)
- 🔰 [Android Application](https://play.google.com/store/apps/details?id=com.programiz.learnpython)
- 🔰 [IOS Application](https://apps.apple.com/app/apple-store/id1472188189?mt=8)

[![image](https://user-images.githubusercontent.com/44474792/123523554-da192a00-d6e1-11eb-887c-abcbf107c70b.jpg)](https://www.programiz.com/python-programming)

### ⭐️ Codecademy

**[Codecademy](https://www.codecademy.com/)** is an American online interactive platform that offers free coding classes in 12 different programming languages including Python, Java, Go, JavaScript, Ruby, SQL, C++, C#, Swift, and Sass, as well as markup languages HTML and CSS. 

[![image](https://user-images.githubusercontent.com/44474792/123522719-bd2e2800-d6dc-11eb-9175-3c9c62e44f9c.jpg)](https://www.hackerrank.com/domains/python)

#

### ⭐️ Snakify

**[Snakify](https://snakify.org/en/)** offers an interactive manual of Python 3 programming language. They offers course from the beginning that is way different from the others. It gives a platform which contains the theory portions of Python from the very beginning and the editors to practice every portions.

![Snakify1](https://user-images.githubusercontent.com/81372148/136075464-64d1c4d6-8a82-46fd-93fa-647517d2fbb2.png)

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

## **7.Hangman Game**

### **Source code**

```ino
import random 
def hangman() :
     
    list_of_words=['python','java','inovus','india','zebra']
    word = random.choice(list_of_words)
    turns = 10
    guessmade = ''
    valid_entry = set('abcdefghijklmnopqrstuvwxyz')

    while len(word) > 0:
        main_word=""
        for letter in word:
            if letter in guessmade:
               main_word= main_word + letter
            else:
                main_word = main_word + "_ "
        if main_word ==word:
            print(main_word)
            print("You Won!!")
            break
        
        print("Guess the words ",main_word)
        guess = input()

        if guess in valid_entry:
            guessmade = guessmade + guess
        else:
            print("Enter a valid entry")
            guess= input()

        if guess not in word:
            turns= turns-1

            if turns==9:
                 print("9 turns left!!")
                 print("-------------------")
               
            if turns==8:
                print("8 turns left!!")
                print("-------------------")
                print("        O          ")
            if turns==7:
                print("7 turns left!!")
                print("-------------------")
                print("        O          ")
                print("        |          ")
            if turns==6:
                print("6 turns left!!")
                print("-------------------")
                print("        O          ")
                print("        |          ")
                print("       /           ")
            if turns==5:
                print("5 turns left!!")
                print("-------------------")
                print("        O          ")
                print("        |            ")
                print("       / \          ")
            if turns==4:
                print("4 turns left!!")
                print("-------------------")
                print("       \O          ")
                print("        |            ")
                print("       / \          ")
            if turns==3:
                print("3 turns left!!")
                print("-------------------")
                print("       \O/          ")
                print("        |            ")
                print("       / \          ")
            if turns==2:
                print("2 turns left!!")
                print("-------------------")
                print("       \O/ |          ")
                print("        |            ")
            
                print("       / \          ")
            if turns==1:
                print("1 turn left!!")
                print("-------------------")
                print("       \O/_|          ")
                print("        |            ")
                print("       / \          ")
            if turns==0:
                print("You Lose!!")
                print("Oops, The Hangman Game is over")
                print("The correct word was",word)
                print("------------------------")
                print("          O_|          ")
                print("         /|\            ")
                print("         / \          ")
                break
                                
name=input("PLEASE ENTER YOUR NAME")
print("Welcome",name ,"!!")
print("---------------------------")
print(name,",Try to guess the word in less than 10 attempts")
hangman()
```
## **Output**
![Hangman 1](https://user-images.githubusercontent.com/81381146/136016743-ebe9bcd7-88c5-42a8-981f-b8a2a8961c81.png)
![Hangman 2 png](https://user-images.githubusercontent.com/81381146/136016749-803e0cf9-56ea-4b7e-9ebd-39e4fa60c082.png)


