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
