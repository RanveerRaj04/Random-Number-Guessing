# Random-Number-Guessing
This code will guess a number between 1 and 100. The code has already chosen a number and the user has to guess it . When we chose the correct number, the program ends and it shows the number of guesses at last.

#guessing a random number
import random
low_num = 1
high_num = 100
guesses= 0

answer = random.randint(low_num,high_num)
answer = int(answer)
is_running = True

while is_running:
    guess = input(f"Guess a number between {low_num} and {high_num} :")
    if guess.isdigit():
        guess = int(guess)
        guesses += 1
        if guess<low_num or guess>high_num:
            print("please feed your integer in the valid range")

        elif guess-answer ==5:
            print("you are just higher than the answer")
        elif guess-answer ==-5:
            print("you are just lower than the answer")
        elif guess-answer ==20:
            print("you are higher than the answer")
        elif guess-answer ==-20:
            print("you are lower than the answer")
        elif guess-answer<-20:
            print("you are very low")
        elif guess-answer>20:
            print("you are very high")
        else:
            print(f"Gotcha! You got it in {guesses} attempts")
            is_running=False


    else:
        guess = input(f"Guess a number between {low_num} and {high_num}")
