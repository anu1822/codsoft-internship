# codsoft-internship
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

#Write your code below this line 👇
import random
game_images = [rock, paper, scissors]

user_choice = int(input("What do you choose? Type 0 for rock, 1 for paper, and 2 for scissors \n"))
print(game_images[user_choice])
if user_choice >=3 or user_choice < 0:
    print("You type an invalid number , You lose..")
else:
    game_images[user_choice]

computer_choice = random.randint(0,2)
print(f"Computer chose {computer_choice}")
print(game_images[computer_choice])
if computer_choice > user_choice:
    print("you lose..")
elif computer_choice == 0 and user_choice == 2:
    print("you lose..")
elif computer_choice == 2 and user_choice == 0:
    print("You win!!")
elif computer_choice == user_choice:
    print("It's a draw")
elif computer_choice == 0 and user_choice ==1:
    print("You win!!")
elif computer_choice == 1 and user_choice == 2:
    print("You win!!")
