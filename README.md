# Hangman Word Game

A simple console-based Hangman Word Game developed using Python. This project allows users to guess a randomly selected word letter by letter through a simple command-line interface.

## 📌 Project Description

The Hangman Word Game is a Python-based application designed to demonstrate basic Python programming concepts through an interactive word-guessing game.

The project is useful for beginners to understand how functions, loops, conditional statements, lists, file handling, random selection, regular expressions, user input, and input validation can be used together to create a simple real-world application.

## 🚀 Features

* Randomly select a word from a word list
* Allow the user to guess one letter at a time
* Display correctly guessed letters
* Hide letters that have not been guessed
* Provide a maximum of 6 incorrect attempts
* Prevent the user from entering more than one character
* Validate that the input contains only letters from A-Z
* Prevent the user from guessing the same letter again
* Display a message for correct guesses
* Display a message for incorrect guesses
* Detect when the complete word has been guessed
* Display the correct word when the player loses
* Read words from an external `words.txt` file
* Handle missing `words.txt` file safely

## 🛠️ Technologies Used

* Python 3
* Random Module
* Regular Expressions (`re`)
* File Handling
* Console / Command-Line Interface

## 🧠 Python Concepts Used

* Functions
* Variables
* Lists
* `for` Loop
* `while` Loop
* `if-elif-else`
* Conditional Statements
* User Input
* String Manipulation
* File Handling
* `try-except`
* Exception Handling
* Input Validation
* Random Word Selection
* Regular Expressions
* Function Calling
* Boolean Values

## 📁 Project Structure

```text
Hangman-Word-Game/
│
├── hangman.py
├── words.txt
└── README.md
```

## ▶️ How to Run

### 1. Install Python

Make sure Python 3 is installed on your computer.

### 2. Clone the Repository

```bash
git clone https://github.com/your-username/Hangman-Word-Game.git
```

### 3. Open the Project Folder

```bash
cd Hangman-Word-Game
```

### 4. Make Sure `words.txt` Exists

The program reads the possible words from a file named:

```text
words.txt
```

Each word should be written on a separate line.

Example:

```text
python
computer
programming
college
student
```

### 5. Run the Program

```bash
python hangman.py
```

## ⚙️ How It Works

* The program starts by reading words from the `words.txt` file.

* A random word is selected from the available words.

* The selected word is stored as the secret word.

* The player starts with 6 attempts.

* The program displays underscores for letters that have not been guessed.

* The player enters one letter.

* The program validates the entered letter.

* If the letter is present in the secret word, it is displayed.

* If the letter is not present, one attempt is removed.

* The program continues until the player guesses the complete word or runs out of attempts.

* If the complete word is guessed, the player wins.

* If all 6 attempts are used, the game ends and the correct word is displayed.

## 🎮 Game Operations

### 1. Select a Secret Word

The program uses Python's `random` module to randomly select a word from the `words.txt` file.

```python
secret_word = random.choice(words)
```

This makes each game different because the secret word can change each time the program runs.

### 2. Display the Word

The `display_word()` function displays the letters that have already been guessed.

For example, if the secret word is:

```text
python
```

and the user has guessed:

```text
p, t
```

the program displays:

```text
p___t_
```

Letters that have not been guessed are represented using `_`.

### 3. Enter a Guess

The `get_guess()` function asks the user to enter a letter.

The program checks whether:

* The user entered exactly one character.
* The character is a letter from A-Z.
* The letter has not already been guessed.

If the input is invalid, the program asks the user to enter another letter.

### 4. Correct Guess

If the guessed letter exists in the secret word, the program displays:

```text
Good guess
```

The guessed letter is then displayed in its correct position.

### 5. Wrong Guess

If the guessed letter does not exist in the secret word, the program displays:

```text
Wrong guess
```

The number of remaining attempts is decreased by one.

The player has a maximum of:

```text
6 attempts
```

### 6. Winning the Game

The `is_word_guessed()` function checks whether every letter in the secret word has been guessed.

If all letters have been guessed, the program displays:

```text
Congratulations! You guessed the word
```

### 7. Losing the Game

If the player uses all 6 attempts without guessing the complete word, the program displays:

```text
Game over! The word was <secret_word>
```

## ⚠️ Error Handling

The program handles different types of invalid input.

For example:

### Multiple Characters

If the user enters:

```text
abc
```

the program displays:

```text
Enter only one letter.
```

### Numbers or Special Characters

If the user enters:

```text
5
```

or:

```text
@
```

the program displays:

```text
Enter only letters from a to z.
```

### Repeated Letter

If the user guesses the same letter again, the program displays:

```text
You already guessed that letter.
```

### Missing Word File

If `words.txt` does not exist, the program catches the `FileNotFoundError` and displays:

```text
words.txt does not exist.
```

## 🔮 Future Improvements

* Add a graphical user interface (GUI)
* Add different difficulty levels
* Add a Hangman drawing after every wrong attempt
* Add a scoring system
* Add a timer
* Add categories such as Animals, Countries, Movies, and Technology
* Add multiple rounds
* Add a leaderboard
* Add hints for difficult words
* Add sound effects
* Add player names
* Store scores permanently
* Add multiplayer functionality
* Add a larger word database

# Hangman Word Game

**Integrated Skills:** Python Programming, File Handling, Input Validation and Problem Solving

## 🎓 Purpose

This project is created for educational and learning purposes.

It demonstrates how basic Python programming concepts can be combined to develop a simple Hangman word-guessing game.

The project focuses on understanding:

* Functions
* Lists
* Strings
* Loops and Conditions
* File Handling
* Random Module
* Regular Expressions
* Input Validation
* Exception Handling
* Basic Application Structure

## 📚 Learning Outcomes

After completing this project, beginners can understand how to:

* Create and use Python functions
* Read data from an external text file
* Select random elements using Python's `random` module
* Store data using lists
* Work with strings
* Validate user input
* Use loops to repeatedly execute a program
* Handle errors using exceptions
* Use regular expressions for input validation
* Build an interactive console application
* Separate different parts of the program into functions

## 🏗️ Project Architecture

The project contains several functions that are responsible for different parts of the game.

### `read_words()`

The `read_words()` function is responsible for reading words from the `words.txt` file.

It includes:

* Opening the word file
* Reading the words
* Removing line breaks
* Returning the list of words
* Handling a missing file

### `display_word()`

The `display_word()` function displays the current progress of the secret word.

It checks each letter of the secret word and displays:

* The actual letter if it has been guessed
* `_` if the letter has not been guessed

### `get_guess()`

The `get_guess()` function handles user input.

It checks:

* Input length
* Whether the input is a letter
* Whether the letter was already guessed

### `is_word_guessed()`

The `is_word_guessed()` function checks whether all letters in the secret word have been guessed.

It returns:

```text
True
```

when the entire word has been guessed and:

```text
False
```

if any letter is still missing.

### `main()`

The `main()` function controls the overall game.

It is responsible for:

* Loading the words
* Selecting the secret word
* Setting the number of attempts
* Storing guessed letters
* Running the main game loop
* Checking guesses
* Determining whether the player wins or loses

## 🔄 Basic Flow

```text
Start
  ↓
Read words from words.txt
  ↓
Check whether words are available
  ↓
Select a random secret word
  ↓
Set attempts = 6
  ↓
Display the hidden word
  ↓
Ask the user for a letter
  ↓
Validate the input
  ↓
Check whether the letter was already guessed
  ↓
Add the letter to guessed letters
  ↓
Is the letter in the secret word?
       ↓
   ┌───┴───┐
   ↓       ↓
  Yes      No
   ↓       ↓
Good      Wrong
Guess     Guess
   ↓       ↓
Check     Decrease
word      attempts
   ↓       ↓
   └───┬───┘
       ↓
Is the complete word guessed?
       ↓
   ┌───┴───┐
   ↓       ↓
  Yes      No
   ↓       ↓
  Win   Attempts > 0?
           ↓
       Continue Game
           ↓
       Game Over
```

## 💡 Example Game

```text
Enter a letter: p
Good guess

p_____

Enter a letter: y
Good guess

py____

Enter a letter: z
Wrong guess

py____

Enter a letter: t
Good guess

pyth__
```

The player continues guessing until the word is completely revealed or all 6 attempts are used.

## 📖 Project Highlights

This project provides practical experience with Python programming and demonstrates how different Python concepts can be combined to create an interactive word game.

The program separates different responsibilities into individual functions such as reading words, displaying the current word, getting user input, and checking whether the word has been guessed.

This makes the program easier to understand, maintain, and improve.

## 👨‍💻 Author

YASHASVI RANAWAT
INTEGRATED MTECH COMPUTATIONAL AND DATA SCIENCE
VIT BHOPAL UNIVERSITY

## 📄 License

This project is created for educational and learning purposes.
