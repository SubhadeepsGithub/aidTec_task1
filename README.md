# aidTec_task1
import random # importing random module so that system can generate a random number.
def game_play(): #defining function for the game 
    print("Welcome to the Game!") #Greetings for the player
    name=input("Enter your name:") #For entering the user name
    print("Giving the rules:\n 1. This game deals with guessing numbers \n 2. The players will be alloted a maximum of 10 attempts to guess the number right\n 3. If player guesses the number right in 10 attempts then he/she will be declared winner\n 4. Players cannot exit the game in the middle")
    #Displays all the rules of the game.
    system_num=random.randrange(1,100)  #stores a random number in the range 1 to 100. User need to guess this number
    attempts=0  #initial value of attempt
    max_attempts=10  #maximum attempts allowed for the user
    while attempts<max_attempts:
        guess_num=int(input("Enter the number:")) #user enters a number
        attempts+=1
        if guess_num<system_num: #entered number is less in amplitude then the system number
            print("Guess is low")
            
        elif guess_num>system_num: #entered number is more in amplitude then the system number
            print("Guess is high")
        
        elif guess_num==system_num: #entered number is equal in amplitude then the system number
            print("You are the Winner!!")
            break
        
        else:
            print("You are out of attempts\n Correct number:",system_num) #maximum attempts already covered
    
def play_again(): #function for alloying the user to play again.
    while True:  #continues until false 
        choice=input("Do you want to play again:\n (yes/no):")
        if choice=="yes":
            game_play() #previous codes start working again
        elif choice=="no":
            print("Okay,you can leave:\n Do join again") #Ending greeting for the user
            break

game_play() #calling method
play_again()#calling method
