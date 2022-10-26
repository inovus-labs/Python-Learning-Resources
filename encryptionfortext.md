# Encrypt and Decrypt Texts

A small python program that encodes and decodes text.

## Prerequisites

- pycryptodome 3.9.8

- Python 3

```ino
from Crypto.Cipher import AES
from Crypto import Random 
from binascii import b2a_hex
import sys

plain_text = sys.argv[1]

key = b'this is a 16 key'

iv = Random.new().read(AES.block_size)


Use key and iv to initialize AES object, use MODE CFB mode

mycipher AES.new(key, AES.MODE_CFB, iv)

# Add iv (key vector) to the beginning of the encrypted ciphertext

# and transmit it together

ciphertext = iv + mycipher.encrypt(plain text.encode())

 mydecrypt = AES.new(key, AES. MODE CFB, ciphertext[:16])



decrypttext = mydecrypt.decrypt (ciphertext[16:])

#output

file_out = open("encrypted.bin", "wb") file out.write(ciphertext[16:])

file_out.close()

print("The key k is: ", key)

print("iv is: ", b2a_hex(ciphertext)[:16])

print("The encrypted data is: ", b2a_hex(ciphertext) [16:])

print("The decrypted data is: ", decrypttext.decode())