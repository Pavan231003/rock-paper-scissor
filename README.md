# rock-paper-scissor
from random import choice

probability = "r,p,s"
probability = probability.split(",")


def game():
    computer_choice = choice(probability)
    user_choice = input("Make the choice from Rock for 'r' , Paper for 'p' and scissor for 's' \n")
    print(computer_choice)
    if (user_choice == 'r' and computer_choice == 'p') or (user_choice =='p' and computer_choice == 's') or (user_choice == 's' and computer_choice == 'r'):
        print("You Lost")
    elif user_choice == computer_choice:
        print("Draw")
    elif (user_choice == 'r' and computer_choice == 's') or (user_choice == 'p' and computer_choice == 'r') or (user_choice == 's' and computer_choice == 'p'):
        print("You Won")
    else:
        print("plz check given Instruction")

    play_again = input("Do You want to play Again.Press y for yes or n fo no ")
    if play_again == "y":
        game()
    elif play_again == "n":
        print("See you Later")
    else:
        print("plz check what you have typed")
        game()

game()






