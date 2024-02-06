# Fhenix
Testing for Fhenix
import random

def roll_dice():
    return random.randint(1, 6)

def rumble():
    player1_score = 0
    player2_score = 0

    rounds = 3

    for round in range(rounds):
        input("Press Enter to roll the dice...")
        
        player1_roll = roll_dice()
        player2_roll = roll_dice()
        
        print(f"Player 1 rolled: {player1_roll}")
        print(f"Player 2 rolled: {player2_roll}")
        
        if player1_roll > player2_roll:
            print("Player 1 wins this round!")
            player1_score += 1
        elif player2_roll > player1_roll:
            print("Player 2 wins this round!")
            player2_score += 1
        else:
            print("It's a tie!")
    
    print("\nFinal Scores:")
    print(f"Player 1: {player1_score}")
    print(f"Player 2: {player2_score}")

    if player1_score > player2_score:
        print("Player 1 wins the game!")
    elif player2_score > player1_score:
        print("Player 2 wins the game!")
    else:
        print("It's a tie!")

if __name__ == "__main__":
    rumble()
