# TAS-
import random

def guess_number():
    # Generate a random number between 1 and 100.
    target_number = random.randint(1, 100)

    # Initialize the number of attempts and score.
    attempts = 0
    score = 0

    # Keep looping until the user guesses the correct number or reaches the maximum number of attempts.
    while attempts < 10:
        # Prompt the user to guess the number.
        guess = int(input("Guess a number between 1 and 100: "))

        # Increment the number of attempts.
        attempts += 1

        # Compare the user's guess with the target number.
        if guess == target_number:
            # The user guessed correctly!
            print("Congratulations! You guessed the number in {} attempts.".format(attempts))
            score += 100 - attempts
            break
        else:
            # The user guessed incorrectly.
            if guess > target_number:
                print("Your guess is too high.")
            else:
                print("Your guess is too low.")

    # Display the final score.
    print("Your final score is {}.".format(score))

if __name__ == "__main__":
    guess_number()
