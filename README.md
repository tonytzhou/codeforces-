# Documenting my Competetive Progamming Journey
After having a class in school that focused a lot on solving some coding problems to learn how to implements different data structures, I wanted to dabble in competetive progamming in order to improve my skills. By creating and managing this repository, I hope to track my progress while also being familiar with github. I hope to see improvements in not just my code, competetiveness and rank, but also gaining valuable skills and intution that is necessary as a CS major.

# Documenting my Competetive Progamming Journey
Current Rating:

# Easy
**Team** - Extremely easy, just need to take in a bool of 3 numbers and check if 2/3 are true<br>

**Lost in the Shuffle** - For this problem, I simply initialized four integer variables: num swaps for the
number of swaps occurring, the doll position (3), and x and y, showing where
the swaps were going to occur. There isn’t a specific data structure involved in
this as it was just simple swaps that were inputted from the user. Once the doll
was swapped, I updated it to the swapped value and outputted it at the end.
The time complexity of this solution is O(n), where n is the number of swaps. <br>

**Juice Box** - For this problem, I used a multidimensional array to represent a grid resembling
the juice box. After using a double for-loop to input the grid, I used another
double for-loop to iterate through the entire grid, checking if it matched the
desired grid pattern. This was done by comparing the four letters at each index,
and if they all matched, I outputted the coordinates of the top-left corner of
the matching grid. The time complexity of this solution is O(n^2), where n is
the size of the grid, since I used two nested loops to iterate through it. <br>

**The Stairs** - For this problem, I first declared all my integer variables and decided to use two
vectors: one to store the stair heights and another to calculate the differences
between them. After taking in my input, I iterated through the vector and
subtracted the current stair height from the next one, pushing the results into
a diffVector. I then used a variation of the Boyer-Moore algorithm to count
the most frequently occurring number. Unlike the original algorithm, I updated
the count not only when it was 0 but also when it was 1, allowing for multiple
numbers to be the most frequent. After this, I used a for-loop to subtract the
stair heights again and compare the result with the algorithm’s output. If the
answer didn’t match at index i + 1 and i + 2, the wrong stair would be at i + 2.
For edge cases, if i = 0, the problem lay at the beginning, and if neither of
the previous conditions was satisfied, the wrong stair was at the end. The time
complexity of this solution is O(n) due to the Boyer-Moore algorithm iterating
through all the stairs <br>

# Medium


# Hard
