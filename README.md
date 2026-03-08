# Random-Number-Guessing
This code will guess a number between 1 and 100. The code has already chosen a number and the user has to guess it . When we chose the correct number, the program ends and it shows the number of guesses at last.

#random number guessing game
import random

lower_num=1
higher_num=100
guesses=0

answer= random.randint(lower_num,higher_num)
is_running=True

while is_running:
    guess = input(f"Guess a number between {lower_num} and {higher_num} :")

    if guess.isdigit() :
        guess = int(guess)
        guesses+=1

        if guess<lower_num or guess>higher_num:
            print("Your guess is out of range")
        elif guess<answer:
            print("It's low! Try again")
        elif guess>answer:
            print("It's high! Try again")
        else:
            print(f"Correct! The right answer was {guess}")
            is_running=False

    else:
        print("INVALID INPUT")
        guess = input(f"Please select a number between {lower_num} and {higher_num}")

print(f"Number of guesses = {guesses}")
