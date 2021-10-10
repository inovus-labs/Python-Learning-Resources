
## **Hangman Game**

### **What is Hangman Game?**

Hangman game is a simple game for two or more players.This is actually a guessing game where one needs to guess the appropriate word based on number of dashes shown on the screen. As the name suggests, the player has to save the man from getting hanged. For this the player needs to make correct guess. If the guesses are correct then it will be victory. Whenever the player makes incorrect guesses, each part of the hangman will be displayed on the screen also with a warning message that shows the number of remaining turns/chances. If the player failed to guess the word, then that means he let the poor man die!! And that's the end of the game.

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
