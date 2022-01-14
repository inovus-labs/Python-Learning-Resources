## **1) Reverse a String using For Loop**
Here, we call a function to reverse a string, which iterates through every element using **for loop** and joins each character to the beginning so as to obtain the reversed string.

#### **Source Code**
```py
def reverse(s):
  str = ""
  for i in s:
    str = i + str
  return str
  
s = input("\nEnter the string to be reversed: ")
  
print ("\nThe original string  is : ", end="")
print (s)
  
print ("The reversed string is : ", end="")
print (reverse(s))
```

#### **Output**
![image](https://user-images.githubusercontent.com/44474792/148847443-d9f7b4e4-0029-4e55-a812-cd2178334cea.png)


## **2) Encrypt & Decrypt a Message**
Here, we call a function to reverse a string, which iterates through every element using **for loop** and joins each character to the beginning so as to obtain the reversed string.

#### **Source Code**
```py
from cryptography.fernet import Fernet

message = input("Enter the Text to be Encrypted : ")
key = Fernet.generate_key()
fernet = Fernet(key)
encMessage = fernet.encrypt(message.encode())

print("\nThe Original String is : ", message)
print("Key for encryption : ",key)

print("\nEncrypted Message : ", encMessage)
decMessage = fernet.decrypt(encMessage).decode()
print("\nDecrypted Message : ", decMessage)
```

#### **Output**
![image](https://user-images.githubusercontent.com/44474792/149502483-38b06df9-64e4-4463-8c3c-66a7a961b277.png)


## **3) Random Number Generator *(without built-in funtionalities)***
Here, we call a function to reverse a string, which iterates through every element using **for loop** and joins each character to the beginning so as to obtain the reversed string.

#### **Source Code**

```py
import time

def rand_val(x):
  max = int(input("\nEnter the maximum limit : "))
  random = int(time.time() * max/10)
  random %= x
  return random

print("Random Number Generator (Without built-in funtionalities)")
print("Warning : Minimum fixed to '0'")
x = int(time.time())
print("The Random Number is : ", rand_val(x))
```

```py
def test(strs):
  strs.sort()
  return strs

strs = input("Enter the list words be sorted : ")
print("\nThe original list is :", strs)

strs = strs.split(", ")
print("The sorted list is :", test(strs))
print("\nThe sorted order is : ", end = " ")

for x in strs :
  print(x, ",", end = " ")
```

#### **Output**
![image](https://user-images.githubusercontent.com/44474792/149502548-c8d3480c-3931-4a82-8a15-39cb306ab51e.png)