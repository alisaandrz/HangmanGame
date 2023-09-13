Hangman Game
This is a simple implementation of the classic Hangman game in Python. The game randomly selects a word from a predefined list, and the player must guess the letters of the word within a limited number of attempts.

Getting Started
To play the Hangman game, follow these instructions:

Clone the Repository: You can clone this repository to your local machine using the following command:

shell
Copy code
git clone https://github.com/your-username/hangman-game.git
Navigate to the Directory: Change your current directory to the one containing the game files.

shell
Copy code
cd hangman-game
Run the Game: Execute the script by running the following command:

shell
Copy code
python hangman.py
Play the Game: The game will start, and you will be prompted to enter a character to guess the word.

Game Rules
You have a limited number of attempts (default: 5) to guess the word.

The game will display the current state of the word with underscores for unguessed letters. You can see your progress with each correct guess.

If you guess a letter that is in the word, it will be revealed in its correct position(s).

If you guess a letter that is not in the word, you will lose an attempt.

If you correctly guess all the letters in the word, you win the game.

If you run out of attempts without guessing the word, you lose the game.

Customizing the Word List
You can customize the word list by modifying the word_list variable in the code. Add or remove words to change the set of words that the game can randomly select from.

python
Copy code
word_list = ["banana", "watermelon", "cherry", "strawberry"]
Enjoy the Game!
Have fun playing Hangman! Test your word-guessing skills and see if you can guess the hidden words within the given number of attempts. Good luck!





Regenerate
Send a message

        else:
            print("Incorrect guess.")
            attempts_left= attempts_left -1

        #Check if the player has guessed the word correctly
        if display_word == word_to_guess:
           print(f"Congratulations! You guessed the word: {word_to_guess}")
           break
    if attempts_left ==0:
       print(f"Sorry, you ran out of attempts. The actual word is: {word_to_guess}")


main()# HangmanGame
