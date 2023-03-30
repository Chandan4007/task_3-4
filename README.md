#Matrix Word Search Function.
   > The find_word function takes in two parameters: a 2D list of characters matrix, and a string word.
   > It first finds the number of rows and columns in the matrix by calling the len function on the first row and the matrix itself.
   > It then loops through every cell in the matrix using nested for loops, checking each cell to see if it matches the first letter of the target word.
   > If the current cell matches the first letter of the target word, the function checks if the remaining letters of the word can be found in the same row      as the current cell. It does this by checking if the concatenation of the characters in the row, starting from the current cell and extending to the        length of the target word, matches the target word.
   > If the remaining letters of the word cannot be found in the same row as the current cell, the function checks if they can be found in the same column      instead. It does this by creating a new list containing the characters in the column, starting from the current row and extending to the length of the      target word, and checking if its concatenation matches the target word.
   > If either of the previous two steps find a match, the function returns True.
   > If no matches are found, the function returns False.

     Overall, the find_word function checks whether a target word can be found in the matrix by going left-to-right, or up-to-down. It does this by              checking each cell in the matrix and comparing it to the target word.
