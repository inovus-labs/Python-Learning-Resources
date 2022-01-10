## **Rock-Paper-Scissors Game**

### **Source Code**

#### **main.py**
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

### **Output**
![image](https://user-images.githubusercontent.com/44474792/148847443-d9f7b4e4-0029-4e55-a812-cd2178334cea.png)
