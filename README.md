# FirstGame.py
import random # Random module use for computer to choose

comp_choise = random.choice(['w','g','s']) # Here Computer Choose From (water,snake,gun) as (water(w),snake(s),gun(g))

Player = input("Choose: Water as (w) Snake as (s) Gun as (g) ") # Here user can select ((w),(s),(g))

# if both choose same game tie
if comp_choise == Player:  
    game = None

# Computer winning 
elif (comp_choise == 's' and Player == 'w') or (comp_choise == 'g' and Player == 's') or (comp_choise == 'w' and Player == 'g'):
    game = False

# User Winning
else:
    game = True
 
# printing result of game    
if game:
    print(f"You Choose {Player} and Computer choose {comp_choise}\n***********You Win***********")
elif game == None:
    print("Game Tie!")
else:
    print(f"You Choose {Player} and Computer choose {comp_choise}\n***********Computer Win***********")
