 Guess the Number Game

## Description

This is a simple Rust guessing game where the player tries to guess a randomly generated number between 1 and 100.

## How to Play

Run the game using a Rust compiler (cargo run).
The game will prompt you to enter your guess.
Type a number between 1 and 100 and press Enter.
The game will tell you if your guess is too low, too high, or correct.
Keep guessing until you correctly guess the number.
## Code Overview

- Imports:

rand::Rng: Provides functionality for generating random numbers.
std::{cmp::Ordering, io}: Includes modules for comparison operations and input/output.
- Main Function:

Prints a welcome message and a separator for visual clarity.
Generates a secret number between 1 and 100 using rand::thread_rng().gen_range(1..101).
Starts a loop that continues until the correct number is guessed:
Prompts the user to enter their guess.
Reads the user's input as a string
Attempts to parse the string into a u8 integer:
If successful, stores the parsed integer.
If unsuccessful (e.g., non-numeric input), ignores the input and continues the loop.
Prints the user's guess.
Compares the guess to the secret number:
If less, prints "Too small."
If greater, prints "Too big."
If equal, prints "Congratulations, you WIN!" and breaks the loop.
## Additional Notes

The code handles invalid input gracefully by ignoring it and continuing the game.
The game is designed for a single player.
The game could be expanded with additional features, such as:
Tracking the number of guesses
Allowing the player to choose a difficulty level
Providing hints
