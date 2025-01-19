# rock__.paper__.scissor

This is a Python implementation of a **Rock-Paper-Scissors** game.

---

### **1. Constants and Setup**
- **Constants**:
  - `ROCK`, `SCISSORS`, `PAPER`: Represent the three valid choices in the game, defined as `'r'`, `'s'`, and `'p'`.
- **Emojis Dictionary**:
  - Maps each choice to its corresponding emoji for a user-friendly display.
    ```python
    emojis = { ROCK: '🪨', SCISSORS: '✂️', PAPER: '📃' }
    ```
- **Choices Tuple**:
  - `choices = tuple(emojis.keys())`: A tuple containing all valid choices (`'r'`, `'s'`, `'p'`).

---

### **2. Functions**

#### **a. `get_user_choice()`**
- **Purpose**: Prompts the user to input their choice of rock, paper, or scissors.
- **Logic**:
  - Continuously asks for input until the user provides a valid choice (`'r'`, `'p'`, or `'s'`).
  - Converts the input to lowercase to ensure case insensitivity.
- **Validation**:
  - Checks if the input is one of the valid choices in `choices`.
  - If invalid, displays an error message: `'Invalid choice!'`.

---

#### **b. `display_choices(user_choice, computer_choice)`**
- **Purpose**: Displays both the user's and computer's choices using emojis.
- **Implementation**:
  ```python
  print(f'You chose {emojis[user_choice]}')
  print(f'Computer chose {emojis[computer_choice]}')
  ```
  - Accesses the `emojis` dictionary to get the emoji corresponding to the choices.

---

#### **c. `determine_winner(user_choice, computer_choice)`**
- **Purpose**: Determines the outcome of the game (tie, user win, or user loss).
- **Logic**:
  - **Tie**: If the user's and computer's choices are the same.
  - **User Win**: Based on the game rules:
    - Rock beats Scissors.
    - Scissors beats Paper.
    - Paper beats Rock.
  - **User Loss**: If the computer's choice beats the user's choice.

---

#### **d. `play_game()`**
- **Purpose**: Orchestrates the game logic and provides a looping structure to play multiple rounds.
- **Steps**:
  1. Calls `get_user_choice()` to get the player's choice.
  2. Randomly selects the computer's choice using:
     ```python
     computer_choice = random.choice(choices)
     ```
  3. Displays both choices using `display_choices`.
  4. Determines the winner using `determine_winner`.
  5. Prompts the user to decide whether to continue:
     - If the user inputs `'n'`, the game ends.
     - Otherwise, it loops back for another round.

---

### **3. Program Execution**
- The game begins with a call to `play_game()`.
- The user and the computer make their choices.
- The choices are displayed, and the winner is determined.
- The loop continues until the user chooses to exit by typing `'n'`.

---

### **Core Concepts Demonstrated**
1. **Control Flow**:
   - `while` loops for continuous gameplay and input validation.
   - Conditional statements (`if`, `elif`, `else`) for decision-making.

2. **User Interaction**:
   - Input handling and providing feedback to the user.

3. **Randomization**:
   - `random.choice()` simulates the computer's random choice.

4. **Data Structures**:
   - Use of dictionaries (`emojis`) and tuples (`choices`) for efficient data representation.
