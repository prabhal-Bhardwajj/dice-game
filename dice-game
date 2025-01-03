import random
import os
import csv
import time


file_path = r'C:\Users\PRABAL\OneDrive\Desktop\FULL_STACK\python\Dice_results.csv'
#//////////////////////////////////////////////////////////////////////////////////////
def get_dice_art(number):
    dice_art = {
        1: ["┌─────────┐",
            "│         │",
            "│    *    │",
            "│         │",
            "└─────────┘"],
        2: ["┌─────────┐",
            "│  *      │",
            "│         │",
            "│      *  │",
            "└─────────┘"],
        3: ["┌─────────┐",
            "│  *      │",
            "│    *    │",
            "│      *  │",
            "└─────────┘"],
        4: ["┌─────────┐",
            "│  *   *  │",
            "│         │",
            "│  *   *  │",
            "└─────────┘"],
        5: ["┌─────────┐",
            "│  *   *  │",
            "│    *    │",
            "│  *   *  │",
            "└─────────┘"],
        6: ["┌─────────┐",
            "│  *   *  │",
            "│  *   *  │",
            "│  *   *  │",
            "└─────────┘"]
    }
    return dice_art[number]
#/////////////////////////////////////////////////////////////////////////////////////////////////
def display_single_dice(number):
    dice_art = get_dice_art(number)
    for line in dice_art:
        print(line)

#/////////////////////////////////////////////////////////////////////////////////////////////////
def display_dice(player_roll, computer_roll):
    player_dice = get_dice_art(player_roll)
    computer_dice = get_dice_art(computer_roll)
    print("----------------------------------------------")
    for line in player_dice:
        print(line)
    print("|                                            |")
    for line in computer_dice:
        print(line)
    print("-----------------------------------------------")
#////////////////////////////////////////////////////////////////////////////////////////////        

def save_results(file_path, rounds, max_dice_user, min_dice_user, player_score, computer_score):
    """
    Save game results to a CSV file.
    """
    file_exists = os.path.exists(file_path) and os.path.getsize(file_path) > 0
    with open(file_path, mode='a+', newline='') as file:
        writer = csv.writer(file)
        if not file_exists:
            # Write headers if the file doesn't exist
            writer.writerow(["Rounds", "Max Dice User", "Min Dice User", "User Score", "Computer Score"])
        # Write the game data
        writer.writerow([rounds, max_dice_user, min_dice_user, player_score, computer_score])
    print(f"Game results saved to '{file_path}'.")

def dice_game():
    print("\nWelcome to the Dice Rolling Game!\n")
    rounds = int(input("Enter the number of rounds you want to play: "))

    # Initialize scores and rolls list
    player_score = 0
    computer_score = 0
    user_rolls = []  # To track user's rolls

    for i in range(1, rounds + 1):
        print(f"\n--- Round {i} ---")

        # Roll the dice
        print (" WE SHALL ROLL THE DICE NOW !!")
        time.sleep(0.86)
        
        player_roll = random.randint(1, 6)
        computer_roll = random.randint(1, 6)

        # Track user's rolls
        user_rolls.append(player_roll)
        time.sleep(1.05)
        
        print(f"You rolled: {player_roll}")
        display_single_dice(player_roll)
        time.sleep(1.05) 
        
        print(f"Computer rolled: {computer_roll}")
        display_single_dice(computer_roll)
        time.sleep(1)
        # Added 2 January 2025
        display_dice(player_roll, computer_roll)
        # Calculate difference
        difference = abs(player_roll - computer_roll)

        # Assign points
        if difference == 0:
            print("It's a tie! No points awarded.")
        elif player_roll > computer_roll:
            player_score += difference
            print(f"You win this round and get {difference} points!")
        else:
            computer_score += difference
            print(f"Computer wins this round and gets {difference} points!")

        # Print current scores
        print(f"Current Scores -> You: {player_score}, Computer: {computer_score}")

    # Calculate statistics
    max_dice_user = max(user_rolls)
    min_dice_user = min(user_rolls)

    # Game over
    print("\n=== Game Over ===")
    print(f"Your final score: {player_score}")
    print(f"Computer's final score: {computer_score}")
    print(f"Maximum number rolled by you: {max_dice_user}")
    print(f"Minimum number rolled by you: {min_dice_user}")

    # Determine the winner
    if player_score > computer_score:
        print("Congratulations! You won the game!")
    elif player_score < computer_score:
        print("Tough luck! The computer won the game!")
    else:
        print("It's a tie game!")

    # Save results to CSV
    save_results(file_path, rounds, max_dice_user, min_dice_user, player_score, computer_score)

# Run the game
dice_game()
while True:
    inp = input("Press Q to quit or C to Play Again")
    inp = inp.upper()
    if(inp == 'C'):
        dice_game()
    elif ( inp == 'Q'):
        print("Thank you for playing")
        break  
    else:
        print("Enter the valid input")
            

'''
def weighted_dice_roll():
   
    return random.choices([1, 2, 3, 4, 5, 6], weights=[5, 20, 25, 25, 20, 5], k=1)[0]


'''

