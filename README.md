# Rock-Paper-Scissors-Game
Easy to Play Rock Paper Scissors Game
import random

player_score = 0
cpu_score = 0


print("Welcome to my Rock, Paper, Scissors Game!")
print("First to 3 Points wins!")

RPC_list = ["rock", "paper", "scissors"]

while player_score < 3 and cpu_score < 3:
    player_choice = input("Rock, Paper, or Scissors?: ")
    CPU_choice = random.choice(RPC_list)
    
    print("CPU choice: " + str(CPU_choice) + " VS Player: " + str(player_choice))
    
    if player_choice.lower() == CPU_choice:
        print("Tie! No Points!") or print("Tie! Round Over! Back to your Corners!")
    
    elif player_choice.lower() == "rock":
        if CPU_choice == RPC_list[2]:
            player_score += 1
            print("BOOM! Player Wins, rock breaks scissors in two! 1 Point to Player.")
        elif CPU_choice == RPC_list[1]:
            cpu_score += 1
            print("Oh No! CPU Wins, paper covers rock! 1 Point towards CPU.")
    
    elif player_choice.lower() == "paper":
        if CPU_choice == RPC_list[0]:
            player_score += 1
            print("Player wins, the rock can't beat paper! 1 point to Player.")
        elif CPU_choice == RPC_list[2]:
            cpu_score += 1
            print("Uh Oh! CPU Wins. Scissors cuts paper to shreds!, 1 Point to CPU.")
    
    elif player_choice.lower() == "scissors":
        if CPU_choice == RPC_list[1]:
            player_score += 1
            print("Player Wins! Scissors cuts paper into millions! 1 Point to Player!")
        elif CPU_choice == RPC_list[0]:
            cpu_score += 1
            print("Oh No! the rock destroys the scissors! 1 Point to CPU")
    else:
        print("Invalid input! New Round!")


if player_score > cpu_score:
    print("Player wins!")
else:
    print("CPU wins!")
    
    
    #if player_score == 1:
        #print("4 points to go!")
