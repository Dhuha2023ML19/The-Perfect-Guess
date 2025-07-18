# The-Perfect-Guess
import random
randNum=random.randint(0,100)
randNum=random.randint(0,100)


a=None
no_of_guesses=0
while (a!=randNum):
    no_of_guesses+=1
    
    a=int(input("Guess a random number between 0 to 100:"))
    print(f"User entered:{a}")
    
    # print(f"The perfect random number generated: {randNum}")
    if a==randNum:
        print("The perfect guess 🥳")
        print(f"The perfect random number generated: {randNum}")
    else:
        if a>randNum:
            print("Lesser number please!")
        elif a<randNum:
            print("Higher number please!")
    
    


    
print(f"The no of total guesses are: {no_of_guesses}")


with open("Guess.txt","r")as f:
    hiscore=int(f.read())

if (no_of_guesses<hiscore):
    with open("Guess.txt","w")as f:
        print("You have broken the high score!")
        f.write(str(no_of_guesses))

