# Stone-paper-scissor-game
import random
def user_choice():
    user_input = input("Enter your choice (Rock/Paper/Scissors): ")
    if user_input in ["rock", "paper", "scissors"]:
        return user_input.lower()
    else:
        print("Invalid input. Please choose Rock, Paper, or Scissors.")
        return user_choice()
def computer_choice():
    return random.choice(["rock", "paper", "scissors"])
def determine_winner(user_choice, computer_choice):
    if user_choice == computer_choice:
        return "It's a tie!"
    elif ((user_choice == "rock" and computer_choice == "scissors") or 
          (user_choice == "paper" and computer_choice == "rock") or 
          (user_choice == "scissors" and computer_choice == "paper")):
        return "You win!"
    else:
        return "You lose!"
user_play = user_choice()
computer_play = computer_choice()
print("Computer got:", computer_play)
print(determine_winner(user_play, computer_play))
