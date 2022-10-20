# CLI-QR-SCANNER 

## About the project
Its a QR code scanner builded using python. You can use this code in your laptop to run this command line based QR code scanner. It has two operations that you can scan a qr code from a image url or the qr code image in your system also you can scan a qr code lively using your laptop webcamera .

## Requirement
Python 3.10.1

Python Libararies

1) pyzbar -0.1.9
2) opencv-python - 4.6.0.66
3) Numpy - 1.23.1
4) Pillow -  9.0.1

## Code
```ino
import time
import os
import cv2
import numpy as np
import pyzbar.pyzbar as pyzbar
import urllib.request
def script():
    print("Welcome to the Qr code scanner")
    print("Its to use QRs")
    print("How do you want to scan a Qr code")
    print("1.From a Camera")
    print("2.From a Image")
    option=input("Enter your option :")
    n=0
    if option=='1':
        cap = cv2.VideoCapture(0)
        font = cv2.FONT_HERSHEY_PLAIN
        print("Lets Get started")
        while True:
            _, frame = cap.read()

            decodedObjects = pyzbar.decode(frame)
            for obj in decodedObjects:
                print("Data", obj.data)
                cv2.putText(frame, str(obj.data), (50, 50), font, 2,
                    (255, 0, 0), 3)

            cv2.imshow("Frame", frame)

            cv2.waitKey(1)
            n=n+1
            if n == 480:
                break
    elif option=='2':
        print("From where your image is to be scanned")
        print("1.From an local image \n2.From an url")
        sol=input("Choose Your Option (1/2) : ")
        if sol=='1':
                print("Make sure that your image is saved in the folder where this file running")
                time.sleep(40)
                loc=str(input("\n Enter you image name with extension : "))
                image = cv2.imread(loc)
                decodedObjects = pyzbar.decode(image)
                for obj in decodedObjects:
                    print("Type:", obj.type)
                    print("Data: ", obj.data, "\n")
                cv2.waitKey(0)
                print("Thank you :)")
        elif sol=='2':
            source=str(input("Enter you image url: "))
            imag_source = source.split('/')[-1]
            urllib.request.urlretrieve(source,
                imag_source)
            image = cv2.imread(imag_source)
            decodedObjects = pyzbar.decode(image)
            for obj in decodedObjects:
                print("Type:", obj.type)
                print("Data: ", obj.data, "\n")
            cv2.waitKey(0)
            eqn=input("Do you want to delete the image file for qr code (y/n): ")
            if eqn=='y':
                os.remove(imag_source)
                print("Deleted")
            else:
                print("Yeah you can keep it")
            print("Thank you :)")
        else:
            print("Sorry wrong input")
            print("Also some error occured please return to the terminal")
    else:
        print("Wrong Input")
    reset=input("Do you want to continue(y/n):")
    if reset=='y' or reset=='Y':
        script()
    else:
        print("Thank you")
script()
```

## Working
you only needed to execute the code after installing all requirements

Thank you for reading