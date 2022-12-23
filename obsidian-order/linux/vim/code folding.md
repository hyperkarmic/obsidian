# Code Folding
If you are comfortable using the line numbers, the command is even easier to remember: `:5,16fo` (fo stands for code **fo**ld). Once you have folded your code, it’s easy to toggle between open and closed views using `zo` (Open the code fold) and `zc` (Close the code fold). Don’t stress it so much. Just use `za` to toggle between open and closed folds ?

Let’s say you spent considerable time folding your functions in a large file, you would obviously want to retain those folds every time you open that file right? (If not, why did you waste your energy folding them!?), so there’s a solution right in your `~/.vimrc` . Insert the following lines in `~/.vimrc`and your code folds are saved and restored:

#vim #linux #folding #code-folding