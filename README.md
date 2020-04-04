# Snake-Water-Gun
#game

import random
print("chhose one")
print("s for Snake")
print("w for Water")
print("g for Gun")
i=0
s=0
b=0
#a=int(input("enter your choice"))
while(i<10):
    a = str( input( "enter your choice" ) )

    if(a=="s"):
       print("Snake")
       i = i + 1

    elif(a=="w"):
       print("Water")
       i = i + 1
    elif(a=="g"):
        print("Gun")
        i = i + 1
    else:
         print("wrong choice")
         i = i + 1
    lst = ["Snake", "Water", "Gun"]
    computer = random.choice( lst )
    print( "computers choice", computer )
    if(a=="s" and computer=="Water" or a=="g" and computer=="Snake" or a=="w" and computer=="Gun"):
        s=s+1
        print("player  score:",s)
        print("computer score: ",b)
    elif(a=="w" and computer=="Snake" or a=="s" and computer=="Gun" or a=="g" and computer=="Water"):
        print("player score:",s)
        b=b+1
        print("computer score:",b)
    elif(a=="s" and computer=="Snake" or a=="w" and computer=="Water" or a=="g" and computer=="Gun"):
        print("both score 0")

    else:
        ("try again")
#computer turn
# lst=["Snake","Water","Gun"]
# computer=random.choice(lst)
# print( "computers choice",computer)
if(s>b):
    print("player is win by ",s-b,"points")

elif(s<b):
    print("computer is win by ",b-s,"points")
else:
    print("game is tie between player nad computer")
