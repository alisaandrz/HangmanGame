import random

# List of predefined words that the palyers need to guess
word_list= ["banana","watermelon","cherry","strawbery"]

def select_random_word():
    #Select a random word from the list
    return random.choice(word_list)

def initialize_game():
    #Give out all the variables that is needed to execute the game
    word_to_guess= select_random_word()
    display_word= len(word_to_guess)* "_"
    attempts_left= 5 

    return word_to_guess, display_word, attempts_left

def main():
    print("Welcome to the Hangman game!")

    #Intitialize the game
    word_to_guess, display_word, attempts_left= initialize_game()

    while attempts_left>0:
        print(f"Word: {display_word}")
        print(f"Attempts left: {attempts_left}")
        
        #Get user's input of the character
        guess= input("Enter a character:").lower()

        #Check if the character that the player guessed is in the real word
        if guess in word_to_guess:
            print("That's a correct guess!")
            new_display_word=""
            for i in range(len(word_to_guess)):
                if word_to_guess[i] == guess:
                    new_display_word= new_display_word + guess
                else:
                    new_display_word= new_display_word + display_word[i]
            display_word= new_display_word
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
