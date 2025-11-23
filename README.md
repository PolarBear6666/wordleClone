# wordleClone
wordleClone
# Project Title: Wordle Clone (MVC)

## 👤 Team Member
-Huiyuan Zhang

##  How to Run
1.  **Clone repository:** `git clone [Your Repository URL]`
2.  **Ensure Dependencies:** Verify that **Gson 2.10.1** and **JUnit 4.13** are correctly configured in your `pom.xml`.
3.  **Run `Main.java`** in the `wordleclone` package.
4.  **Note on Focus:** If typing does not immediately work, click once anywhere on the game window to ensure the keyboard focus is established.

##  Features Implemented
* **MVC Architecture:** Clean separation into `model`, `view`, and `control`.
* **Core Game Loop:** 6 attempts to guess a 5-letter word.
* **Feedback System:** Implements Green (Correct Position), Yellow (Wrong Position), and Gray (Not in Word).
* **Duplicate Letter Logic:** Correctly handles duplicate letters in both the guess and the secret word.
* **Dictionary Validation:** Guesses are checked against the internal `WordList`.
* **Persistence (Save/Load):** Uses **Gson** and **Java Reflection** to save and load the `WordleModel` state to a `wordle_save.json` file. The game auto-loads the last saved state on startup.
* **Live Typing:** Letters appear on the grid as the user types (Controller $\rightarrow$ View direct communication).
* **Visual Keyboard:** Keys are colored based on their global status (tracked in the Model).

## Controls
| Key | Action |
| :--- | :--- |
| **A-Z Keys** | Input letter for current guess. |
| **Backspace/Delete** | Removes the last letter. |
| **Enter** | Submits the 5-letter guess. |
| **S** | **Save Game** (Saves current state to JSON). |
| **R** | **Reset Game** (Currently displays message, full implementation left for future). |
