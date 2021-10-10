## **2.Rock-Paper-Scissors Game**

## **What is Rock-Paper-Scissors Game?**

Rock paper scissors is a hand game, usually played between two people, in which each player simultaneously forms one of three shapes with an outstretched hand. These shapes are "rock" (a closed fist), "paper" (a flat hand), and "scissors" (a fist with the index finger and middle finger extended, forming a V).  It has only two possible outcomes: a draw, or a win for one player and a loss for the other. A player who decides to play rock will beat another player who has chosen scissors ("rock crushes scissors" or sometimes "blunts scissors"), but will lose to one who has played paper ("paper covers rock"); a play of paper will lose to a play of scissors ("scissors cuts paper"). If both players choose the same shape, the game is tied and is usually immediately replayed to break the tie.

## **Source Code**

### **main.py**
```py
import random
from graphic_view import *
from intro import *
from count import *

def try_again():
    decision = input("Do you want to try again? (Yes/No): ").lower()
    if decision == "y" or decision == "yes":
        print('''
__________________________________________________________________________________________________________________________
        
                                                New Game
                                        ''')
        main()
    elif decision == "n" or decision == "no":
        print("\n*************************************************************************************************************************")
        exit()
    else:
        try_again()

intro()
trial = 3
Pscore = 0
Cscore = 0
def main():
    global Pscore
    global Cscore
    global trial
    if trial >= 1 and (Pscore != 2 and Cscore !=2):
        num = random.randint(1,3)
        print('''__________________________________________________________________________________________________________________________        
Chances Left: ''',trial)
        player = int(input("Enter the number of the shape: "))
        count()
        if num == player:
            print(Tied[player])
            main()
        elif num == 1 and player == 2:
            print(PlayerWins[player])
            Pscore+=1
            trial-=1
            main()
        elif num == 1 and player == 3:
            print(ComputerWins[num])
            Cscore+=1
            trial-=1
            main()
        elif num == 2 and player == 1:
            print(ComputerWins[num])
            Cscore+=1
            trial-=1
            main()
        elif num == 2 and player == 3:
            print(PlayerWins[player])
            Pscore+=1
            trial-=1
            main()
        elif num == 3 and player == 1:
            print(PlayerWins[player])
            Pscore+=1
            trial-=1
            main()
        elif num == 3 and player == 2:
            print(ComputerWins[num])
            Cscore+=1
            trial-=1
            main()
        else:
            print('''
            You have typed wrong value
            Please enter the correct value !!!
            ''')
            main()
    else:
        print(f'''
    _________________________________
    |   Computer     |    Player    |
    |________________|______________|
    |       {Cscore}        |      {Pscore}       |
    |________________|______________|  
    ''')
        if Pscore > Cscore :
            print('''
        !!! You Win The Game !!!

''')
            trial = 3
            Pscore = 0
            Cscore = 0
            try_again()
        else:
            print('''
        !!! You lost the Game !!!

''')
            trial = 3
            Pscore = 0
            Cscore = 0
            try_again()

main()
```

### **graphic_view.py**
```py
scissor = '''
       Computer                                 Player
       _________
      |---------|                            `\.       _
      |---------|                               `\.  ,(_)
      |---------|                                  ::  _
      |---------|                               ,/'  .(_)
      |_________|                            ,/'
         Paper                                  Scissor

                        Player Wins !!!
      
   '''
paper1 = '''
       Computer                                  Player

       _________                               ()()()()() 
      |---------|                             ()()()()()() 
      |---------|                            ()()()()()()()
      |---------|                            ()()()()()()()     
      |---------|                             ()()()()()()  
      |_________|                              ()()()()()
         Paper                                    Rock

                        Computer Wins !!!
      
   '''
paper2 = '''
       Computer                                  Player
       _________                                _________  
      |---------|                              |---------| 
      |---------|                              |---------|
      |---------|                              |---------|     
      |---------|                              |---------|  
      |_________|                              |_________|
         Paper                                    paper

                            Tied !!!
      
   '''
scissor2 = '''
       Computer                                     Player
                                         
       _       ,/'                               `\.       _
      (_).  ,/'                                     `\.  ,(_)
       _  ::                                           ::  _
      (_)'  `\.                                     ,/'  '(_)
               `\.                               ,/'
        Scissor                                     Scissor
                     
                            Tied !!!
   '''
scissor1 = '''

       Computer                                   Player
                                                 _________
       _       ,/'                              |---------|
      (_).  ,/'                                 |---------|
       _  ::                                    |---------|
      (_)'  `\.                                 |---------|
               `\.                              |_________|
        Scissor                                    Paper
                     
                         Computer Wins !!!
   '''
Rock = '''
        Computer                                  Player

                                                ()()()()()
       _       ,/'                             ()()()()()()
      (_).  ,/'                               ()()()()()()()
       _  ::                                  ()()()()()()()
      (_)'  `\.                                ()()()()()()
               `\.                              ()()()()()
        Scissor                                    Rock
                     
                         Player Wins !!!
   '''
Rock2 = '''
        Computer                                   Player

       ()()()()()                                ()()()()()
      ()()()()()()                              ()()()()()()
     ()()()()()()()                            ()()()()()()()
     ()()()()()()()                            ()()()()()()()
      ()()()()()()                              ()()()()()()
       ()()()()()                                ()()()()()
          Rock                                      Rock
                     
                              Tied !!!
   '''
paper = '''
        Computer                                   Player

       ()()()()()                                 _________
      ()()()()()()                               |---------|
     ()()()()()()()                              |---------|
     ()()()()()()()                              |---------|
      ()()()()()()                               |---------|
       ()()()()()                                |_________|
          Rock                                      Paper
                     
                           Player Wins !!!
   '''
Rock1 = ''' 
        Computer                                   Player

       ()()()()()                                
      ()()()()()()                              `\.       _
     ()()()()()()()                                `\.  ,(_)
     ()()()()()()()                                   ::  _
      ()()()()()()                                 ,/'  '(_)
       ()()()()()                               ,/'
          Rock                                     Scissor
                     
                           Computer Wins !!!
   '''
PlayerWins = ["",Rock,paper,scissor]
ComputerWins = ["",Rock1,paper1,scissor1]
Tied = ["",Rock2,paper2,scissor2]
```

### **intro.py**
```py
from graphic_view import *
import time
def intro():
    print('''
***************************************** ROCK PAPER SCISSORS  ******************************************************

                    Instructions
 __________________________________________________
|                                                  |
| * You have 3 chances                             |
| * If you win 2 points then you won the game      |
| * Rock > Scissor                                 |
| * Scissor > Paper                                |
| * Paper > Rock                                   |
| * Who puts the greater shape wins                |
|                                                  |
|                           Developer: Joyel Johny |
|__________________________________________________|

Type the number of the shape below

1.Rock
2.Paper
3.Scissor
    ''')
```

### **count.py**
```py
import time

def count():
    print("")
    for item in ["Rock....","Paper....","Scissor...."]:
        print(item,'\n')
        time.sleep(0.7)
```

## **Output**
![Sample](https://user-images.githubusercontent.com/81413791/136699786-1c4f693b-0d7a-4140-993b-aebe3714f7d6.jpg)


