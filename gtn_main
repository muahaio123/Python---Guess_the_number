import random

logo = """
   ___                       _____ _                __                 _               
  / _ \_   _  ___  ___ ___  /__   \ |__   ___    /\ \ \_   _ _ __ ___ | |__   ___ _ __ 
 / /_\/ | | |/ _ \/ __/ __|   / /\/ '_ \ / _ \  /  \/ / | | | '_ ` _ \| '_ \ / _ \ '__|
/  /_\\| |_| |  __/\__ \__ \  / /  | | | |  __/ / /\  /| |_| | | | | | | |_) |  __/ |   
\____/ \__,_|\___||___/___/  \/   |_| |_|\___| \_\ \/  \__,_|_| |_| |_|_.__/ \___|_|   
                                                                                       
"""
chosen_number = 0
lives = 0

def intro():
    global chosen_number
    
    print(logo)
    print("Welcome to the Number Guessing Game!\nI'm thinking of a number between 1 and 100")
    chosen_number = random.randint(1, 100) # randomize a number from 1 to 100

def choose_difficulty():
    global lives
    
    difficulty = input("Choose a difficulty. Type 'easy' or 'hard': ").lower()
    if difficulty == "easy":
        lives = 10
    else:
        lives = 5

def play_guess():
    global chosen_number
    global lives
    
    guess_num = 0
    while guess_num != chosen_number and lives != 0: # guess the correct number or lose all lives to get out
        print(f"\nYou have {lives} attempts remaining to guess the number.")
        guess_num = int(input("Make a guess: "))

        if guess_num > chosen_number:
            print("Too high.")
            lives -= 1
        elif guess_num < chosen_number:
            print("Too low.")
            lives -= 1
        else:
            break

        if lives != 0:
            print("Guess again.")

    if guess_num == chosen_number:
        print(f"\nCongratulation - You have guessed the correct number: {guess_num}")
    else:
        print(f"\nUnfortunately - You have run out of lives! =(\nThe correct number was: {chosen_number}")

again = 'y'
while again == 'y':
    intro()
    choose_difficulty()
    play_guess()
    again = input("\nWould you like to play another game? Type 'y' for YES | ANYTHING ELSE for NO: ").lower()
