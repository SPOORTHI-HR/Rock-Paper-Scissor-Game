# Rock-Paper-Scissor-Game
Here's a detailed explanation for the Rock-Paper-Scissors game code using Python, which you can include in your README file for GitHub:

---

# Rock-Paper-Scissors Game

This project is a simple implementation of the classic Rock-Paper-Scissors game using Python. The game allows a user to play against the computer with visual representations of each choice.

## Features

- **User vs Computer**: Play the game against the computer.
- **Random Choices**: The computer makes random choices.
- **Visual Representation**: Displays ASCII art for rock, paper, and scissors.
- **Input Validation**: Ensures the user inputs a valid choice.

## Technologies Used

- **Python**: The programming language used to implement the game logic.

## How to Run the Game

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/SPOORTHI-HR/Rock-Paper-Scissor-Game
   ```

2. **Run the Game**:
   ```bash
   python rock_paper_scissors.py
   ```

## Code Explanation

### Python Code

The Python code implements the game logic, including user input, computer choice, and determining the winner. It also includes ASCII art for visual representation.

```python
import random

rock = '''
    ___
---'   __)
      (___)
      (___)
      (__)
---._(__)
'''

paper = '''
    ___
---'   __)_
          ____)
          ______)
         _____)
---.______)
'''

scissors = '''
    ___
---'   _)_
          _____)
       ______)
      (__)
---._(__)
'''

game_images = [rock, paper, scissors]

user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.\n"))
print(game_images[user_choice])

computer_choice = random.randint(0, 2)
print("Computer chose:")
print(game_images[computer_choice])

if user_choice >= 3 or user_choice < 0: 
  print("You typed an invalid number, you lose!") 
elif user_choice == 0 and computer_choice == 2:
  print("You win!")
elif computer_choice == 0 and user_choice == 2:
  print("You lose")
elif computer_choice > user_choice:
  print("You lose")
elif user_choice > computer_choice:
  print("You win!")
elif computer_choice == user_choice:
  print("It's a draw")
```

### Explanation:

1. **Import Libraries**:
   - `random`: Used to generate random choices for the computer.

2. **ASCII Art**:
   - Defines ASCII art for rock, paper, and scissors to visually represent each choice.

3. **Game Images List**:
   - `game_images`: A list containing the ASCII art for rock, paper, and scissors.

4. **User Choice**:
   - Prompts the user to enter their choice (0 for Rock, 1 for Paper, or 2 for Scissors).
   - Displays the corresponding ASCII art for the user's choice.

5. **Computer Choice**:
   - Generates a random choice for the computer (0, 1, or 2).
   - Displays the corresponding ASCII art for the computer's choice.

6. **Determine Winner**:
   - Compares the user's choice and the computer's choice to determine the winner based on the rules of Rock-Paper-Scissors:
     - Rock beats Scissors
     - Scissors beats Paper
     - Paper beats Rock
   - Prints the result of the game (win, lose, or draw).

7. **Input Validation**:
   - Checks if the user entered a valid number (0, 1, or 2). If not, it prints an error message and the user loses.
