This is a personal project meant to optimally solve the "Commander Codex" online game found at https://commandercodex.com/
  Similar to the popular game wordle, you enter guesses and gain information about the hidden answer
  After either 6 wrong guesses or 1 correct one, the game ends

IMPORTANT FUNCTIONS
Fun 1: current_solutions
  - current_solutions is a necessary component for the second function, but has use in its own right
  - Inputs guessed cards and results to output a data frame of all valid solutions left
Fun 2: best_guess
  - best_guess is the primary purpose of this project, as it gives the next best guess for you to make
  - It does so by finding the average number of possible answers removed by a guess
  - Its output is the top 5 guesses based on which removes the most possible answers

INPUT FORMATTING
For both functions, the input is in the form ("CardName1","results1","CardName2","results2",...)
  Card names must be exact (I recommend copy-pasting from CC website)
  Results must be written as 5 upper-case letters, with 3 options for each place
    - The first and last can be Green, Yellow, or Black, so they must be G,Y, or B
    - The 2nd-4th can be Down, Green, or Up, so they must be D,G, or U
ex. best_guess("Edgar Markov", "YDUGB", "Elas il-Kor, Sadistic Pilgrim", "BUDUB")

TROUBLESHOOTING
- If you have only made one guess, leave the other cardname and results spaces blank
- If you want to guess a two-faced card, only guess the front card name eg. "Esika, God of the Tree"
- If the best_guess function has outputted a 1 or 2-row data frame with card characteristics rather than an avg column, that means 2 or fewer answers remain, so there are no calculations to be done
- best_guess can be used to find the best first guess if it is run with no arguments, but be warned that this will take magnitudes longer than anything else
