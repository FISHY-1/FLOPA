import random

def main():
    print("Welcome to the Fishing Game!")
    print("You have 10 attempts to catch as many fish as possible.")

    attempts = 10
    total_fish_caught = 0

    while attempts > 0:
        print(f"\nAttempts left: {attempts}")
        input("Press Enter to cast your line...")
        
        fish_caught = random.randint(0, 3)  # Randomly generate number of fish caught
        total_fish_caught += fish_caught
        attempts -= 1

        if fish_caught == 0:
            print("You didn't catch any fish this time.")
        else:
            print(f"You caught {fish_caught} fish!")

    print("\nGame over!")
    print(f"Total fish caught: {total_fish_caught}")

if __name__ == "__main__":
    main()
Explanation:
Imports: We import the random module to generate random numbers for the fish caught.

Main Function:

The game starts with a welcome message and informs the player that they have 10 attempts.
Inside a while loop (while attempts > 0), the player is prompted to cast their line by pressing Enter.
random.randint(0, 3) is used to simulate catching between 0 to 3 fish per attempt.
The total fish caught is accumulated (total_fish_caught += fish_caught), and attempts are decremented (attempts -= 1).
