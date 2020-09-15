# Snake_Water_Gun_Game-Exercise
Snake, Water and Gun select one and computer select random . See who won !
# # Exercise given by Harry from Code with Harry Youtube Channel (HarisAK)
# Coder - Praveen Singh Chauhan (Technology Video Network - Youtube Channel ,
# GAMP Aaryawarti Films - Film Production & Youtube Channel)
# Link of Youtube - https://www.youtube.com/TechnologyVideoNetwork ,
# https://www.youtube.com/gampaaryawartifilms
# Facebook - https://www.facebook.com/praveen13c
# Twitter - https://twitter.com/praveen13c , https://twitter.com/tvnutube
# Linkedin -  https://www.linkedin.com/in/impraveenchauhan

# Programe Starts
import random  # import random module which is built in

choice_list = ["Snake", "Water", "Gun"]  # variables and assign values
user_win = 0
computer_win = 0
count = 0
tie = 0
s = "Snake"
w = "Water"
g = "Gun"
rest_choice = 10

while count != 10:  # game run 10 times

    print('-' * 30, "Rest chance =", (10-count))  # it shows how many choices left
    print("        Select your option ")
    user_choice = input(" S = Snake  | W = Water  | G = Gun  > ").lower()
    computer_choice = random.choice(choice_list)

    if user_choice == "s" and computer_choice == "Snake" or user_choice == "w" and computer_choice == "Water" \
            or user_choice == "g" and computer_choice == "Gun":  # condition defining here if statement
        count += 1
        tie += 1
        if user_choice == "s":
            print('->' * 20)
            print(f"Tie !!! You select ' {s} ' and computer ' {computer_choice} ' ")
        elif user_choice == "w":
            print('<>' * 20)
            print(f"Tie !!! You select ' {w} ' and computer ' {computer_choice} ' ")
        elif user_choice == "g":
            print('<>' * 20)
            print(f"Tie !!!  You select ' {g} ' and computer ' {computer_choice} ' ")

    elif user_choice == "s" and computer_choice == "Water":
        user_win += 1
        count += 1
        print('<>' * 20)
        print(f"You > {s} Computer > {computer_choice}")
        print(f"You Won  !!!  ")

    elif user_choice == "w" and computer_choice == "Gun":
        user_win += 1
        count += 1
        print('<>' * 20)
        print(f"[ You  > {w} ] | [ Computer  > {computer_choice} ]")
        print(f"You Won  !!!  ")

    elif user_choice == "g" and computer_choice == "Snake":
        user_win += 1
        count += 1
        print('<>' * 20)
        print(f"[ You >  {g} ] | [ Computer  > {computer_choice} ]")
        print(f"You Won  !!!  ")
    elif user_choice == "s" and computer_choice == "Gun":
        computer_win += 1
        count += 1
        print('<>' * 20)
        print(f"[ You  > {s} ] | [ Computer >  {computer_choice} ]")
        print(f"Computer Won  !!!  ")
    elif user_choice == "g" and computer_choice == "Water":
        computer_win += 1
        count += 1
        print('<>' * 20)
        print(f"[ You  > {g} ] | [ Computer > {computer_choice} ]")
        print(f"Computer Won  !!! ")
    elif user_choice == "w" and computer_choice == "Snake":
        computer_win += 1
        count += 1
        print('<>' * 20)
        print(f"[ You  > {w} ] | [ Computer  > {computer_choice} ]")
        print(f"Computer Won  !!! ")
    else:
        print('<>' * 20)
        print("Please enter valid character only")
        print('<>' * 20)
        continue

if user_win > computer_win:  # after game ends , its declare winner
    print("*" * 70)
    print(f"You won {user_win} times and Computer won {computer_win} times and Total Tie {tie}")
    print(f"You WON the GAME !!!!  Total Win = {user_win}")
    print("*" * 70)
else:
    print("*" * 70)
    print(f"You won {user_win} times and Computer won {computer_win} times and Total Tie {tie} ")
    print(f"Computer WON the GAME !!!!!  Total Win = {computer_win}")
    print("*" * 70)
print("!!! Game Ends !!!")
