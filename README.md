# monster-generato
import random #a module (file of prewritten code)

#function definition
def monster(biome):
    num = random.randrange(0, 100)#function call
    if biome == "dungeon":
        if num < 20: #20 percent chance 
            print("A zombie attacks you")
        elif num < 50: #30 percent chance
            print("A skeleton appears!")
        elif num < 90: #40 percent chance
            print("A spier bites you!")
        else: #10 percent chance
            print("a witch throws a potion at you")
    elif biome == "desert":
        if num < 40: #40 percent chance 
            print("A husk attacks you")
        elif num < 60: #20 percent chance
            print("A skeleton appears!")
        elif num < 80: #20 percent chance
            print("A spider bites you!")
        else: #20 percent chance
            print("a witch throws a potion at you")
    elif biome == "ocean":
        if num < 25: #25 percent chance 
            print("A water zombie attacks you")
        elif num < 75: #50 percent chance
            print("A siren appears!")
        elif num < 85: #10 percent chance
            print("A shark bites you!")
        else: #15 percent chance
            print("a witch throws a potion at you")
         
room = 1
while True:
    if room == 1:
        print("You are in room 1. You can go 'n' or 'e'.")
        choice = input()
        if choice == 'e':
            room = 2
        elif choice == 'n':
            room = 4
        else:
            print("not an option dummy")
    if room == 2:
        monster("desert") #function call
        print("You are in room 2. You can go 'n' or 'w'")
        choice = input()
        if choice == 'w':
            room = 1
        elif choice == 'n':
            room = 3
        else:
            print("not an option, dummy")
            
