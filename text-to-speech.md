# Text to Speech

When executed the text file will be turned in to an mp3,saved, and then played on your device.

 ## Prerequisites

 -  abc.txt with your text
 - pip install gTTS
 - pip install os

 ## Code

 ```ino
 from gtts import gTTS
 import os
 file=open("abc.txt","r").read()
 speech=gTTS(text=file, lang='en', slow=False)
 speech.save("voice.mp3")
 os.system("voice.mp3")
 ```
 