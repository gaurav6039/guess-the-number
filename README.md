# guess-the-number
import random

def guess_the_number():
    """
    Plays a 'Guess the Number' game where the computer thinks of a number,
    and the user tries to guess it.
    """
    secret_number = random.randint(1, 20)  # Computer chooses a random number between 1 and 20
    attempts = 0

    print("I am thinking of a number between 1 and 20.")
    print("Can you guess it?")

    while True:
        try:
            user_guess = int(input("Enter your guess: "))
            attempts += 1

            if user_guess < secret_number:
                print("Too low! Try again.")
            elif user_guess > secret_number:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed the number {secret_number} in {attempts} attempts.")
                break
        except ValueError:
            print("Invalid input. Please enter a whole number.")

if __name__ == "__main__":
    guess_the_number()
