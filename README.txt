This is a personal project meant to help optimally solve the "Commander Codex" online game
  Similar to the popular game wordle, you enter guesses and gain information about the hidden answer
  After either 6 wrong guesses or 1 correct one, the game ends

IMPORTANT FUNCTIONS
Fun 1: left_after_guess
  left_after_guess is a necessary component for the second function, but has use in its own right
  Inputs guessed cards and results to output all possible left over options
Fun 2: best_guess
  best_guess is the primary purpose of this project, as it gives the next best guess for you to make
  It does so by finding the average number of possible answers removed by a guess
  Its output is the top 5 guesses on the metric of which removes the most possible answers

READ IF THE FUNCTIONS ARE NOT WORKING AS INTENDED
For both functions, the input is in the form ("CardName1","results1","CardName2","results2",...)
Card names must be exact (eg. "Go-Shintai of Life's Origin" or "Raggadragga, Goreguts Boss")
Results must be written as 5 upper-case letters, with 3 options for each place
  The first and last can be Green, Yellow, or Black, so they must be G,Y, or B
  The 2nd-4th can be Down, Green, or Up, so they must be D,G, or U
  ex. "GDUGG", "YGDDB", "BUGUB"
If you have only made one guess, leave the other cardname and results spaces blank
If you want to guess a two-faced card, only guess the front card name like "Esika, God of the Tree"
