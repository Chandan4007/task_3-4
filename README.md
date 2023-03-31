#Matrix Word Search Function.
   1 The find_word function takes in two parameters: a 2D list of characters matrix, and a string word.
   2 It first finds the number of rows and columns in the matrix by calling the len function on the first row and the matrix itself.
   3 It then loops through every cell in the matrix using nested for loops, checking each cell to see if it matches the first letter of the target word.
   4 If the current cell matches the first letter of the target word, the function checks if the remaining letters of the word can be found in the same row      as the current cell. It does this by checking if the concatenation of the characters in the row, starting from the current cell and extending to the        length of the target word, matches the target word.
   5 If the remaining letters of the word cannot be found in the same row as the current cell, the function checks if they can be found in the same column      instead. It does this by creating a new list containing the characters in the column, starting from the current row and extending to the length of the      target word, and checking if its concatenation matches the target word.
   6 If either of the previous two steps find a match, the function returns True.
   7 If no matches are found, the function returns False.

     Overall, the find_word function checks whether a target word can be found in the matrix by going left-to-right, or up-to-down. It does this by              checking each cell in the matrix and comparing it to the target word.


#Course Order Algorithm

    1.We define a function find_order that takes a dictionary courses as its argument. This dictionary maps each course ID to a list of prerequisites.

    2.We create an empty dictionary graph to represent the graph of dependencies between courses.

    3.We iterate over each course ID in the courses dictionary and create a set of its prerequisites, which we add as a value to the corresponding key in       the graph dictionary.

    4.We create a list roots of nodes that have no dependencies, i.e., nodes with empty prerequisite sets.

    5.We create an empty list order to hold the final ordering of courses.

    6.We enter a loop that continues until there are no more nodes with no dependencies left in the roots list.

    7.Inside the loop, we remove a node node from the end of the roots list.

    8.We add node to the end of the order list, since it has no dependencies and can be completed.

    9.We iterate over each course ID in the graph dictionary, and if node is a prerequisite for that course, we remove it from the prerequisite set.

    10.If the prerequisite set for a course becomes empty after removing node, we add that course to the roots list, since it can now be completed.

    11.We check if the length of the order list is equal to the length of the courses dictionary. If they are not equal, it means that there is a cycle          in the graph, and we return None.

    12.If the lengths are equal, we return the order list, which represents a valid ordering of courses. 
                     or
                     
    1. Define a function called sortCourseId that takes in one argument courseId.

    2. Create an empty list called a.

    3. Loop through each key k in the courseId dictionary.

    4. For each key k, create a tuple v consisting of the key k and the length of its corresponding value in the courseId dictionary.

    5. Append this tuple v to the list a.

    6. Sort the list a based on the second item in each tuple (i.e., the length of the corresponding value).

    7. Create a new list called b that contains only the first item of each tuple in the sorted list a.

    8. Return the sorted list b.

    9. Define a dictionary called courseId with three keys (CSC300, CSC200, CSC100) and their corresponding values.

        Call the sortCourseId function with courseId as the argument.

        Store the returned sorted list in a variable called result.

        Print the result.                
