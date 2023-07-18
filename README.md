# WORDLE GAME
This is a simple command-line game, similar to the board game Mastermind. The program will generate a random 5 to 8-letter word and the user will have a certain number of tries to guess the word.

The program will first prompt the user to enter a word of the correct length (5 to 8 letters). Then, it will check the user's input against the randomly generated word and display feedback for the user. The user's input will be scored according to the number of letters that are in the correct position (green), the number of letters that are in the word but in the wrong position (yellow), and the number of letters that are not in the word (red).

If the user is able to guess the word within the allowed number of tries, they win. If they are unable to guess the word, they lose and the correct word is revealed.

## Usage

```sh
./wordle wordsize
```

where wordsize is the length of the word to guess, which must be 5, 6, 7, or 8.

## Compilation
This program requires the **'cs50'** library, which can be installed as follows:

```sh
$ sudo apt install libcs50
```

Compile using the following command:

```sh
$ clang -o wordle wordle.c -lcs50
```

## User-defined functions
1. **'get_guess(int wordsize)'**: takes an integer as input, which is the length of the word to guess. The function prompts the user to enter a word of the correct length and returns the input as a string.
2. **'check_word(string guess, int wordsize, int status[], string choice)'**: takes four inputs: the user's guess, the length of the word to guess, an integer array to store the score for the guess, and the correct word. The function compares the user's guess to the correct word and returns the score for the guess.
3. **'print_word(string guess, int wordsize, int status[])'**: takes three inputs: the user's guess, the length of the word to guess, and the integer array storing the score for the guess. The function prints the user's guess with colors according to the score.

## Acknowledgements
This program was originally created by David J. Malan for [CS50](https://cs50.harvard.edu/x/2023/psets/2/wordle50/).