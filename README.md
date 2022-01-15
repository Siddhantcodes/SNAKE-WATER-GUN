# SNAKE-WATER-GUN
# An interesting game using basics of python programming.


import random

def gameWin(comp, you):

    if comp == you:
        return None

    elif comp == 's':
        if you == 'w':
            return False
        elif you == 'g':
            return True
    
    elif comp == 'w':
        if you == 'g':
            return False
        elif you == 's':
            return True

    elif comp == 'g':
        if you == 's':
            return False
        elif you == 'w':
            return True
    


print ("Comp turn : Snake(s), Water(w) , Gun(g)??")
r = random.randint(1,3)
if r == 1:
    comp ='s'
elif r == 2:
    comp = 'w'
elif r == 3:
    comp ='g'


you= input("Snake(s), Water(w) , Gun(g) ??")


print(f"Computer chose: {comp}")
print (f"You chose {you}")

s = gameWin(comp,you)

if s == None:
    print ("The game is a tie")
elif you:
    print("You win")
else:
    print ("You lose")

 



  
