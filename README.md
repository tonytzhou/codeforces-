# Documenting my Competetive Progamming Journey
After having a class in school that focused a lot on solving some coding problems to learn how to implements different data structures, I wanted to dabble in competetive progamming in order to improve my skills. By creating and managing this repository, I hope to track my progress while also being familiar with github. I hope to see improvements in not just my code, competetiveness and rank, but also gaining valuable skills and intution that is necessary as a CS major. 

# Difficulty Documentation
The way I seperate the difficulty correlates to the amount of time and thinking that I spent on the problem, so although some problems may not be that difficult/code is not that complex, it may be in the medium/hard difficulty. This also applies to easy ones that may have longer code but less time spent on it.

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

**Chocolate Frogs** - For this problem, I used a hash map to store the input card values. This
structure was particularly useful because it allowed me to track the occurrences
of each card efficiently. After populating the hash map, I simply outputted the
first value (the card) and the second value (the number of occurrences). Input
operations took O(1) time, but traversing the hash map to get the values likely
took O(n) time.

# Medium
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

# Hard
**Wizard Chess** - For this
problem I employed the usage of BFS and tuples. I decided to use the pair data
structure as I knew that there were two values that I would need to keep track
of, the row and column. I took in the input but also subtracted it by ‘a’ and ‘1’
in consideration of the ascii value and making it easier to work with and being
able to use an 8x8 grid to display it. After this, I called my BFS algorithm
which takes in the starting square, ending square, blocked squares, and the way
the knight can move. I used a multidimensional array in order to keep track of
all the values that were visited and blocked, initializing certain values to true
to represent it. In order to keep track of the path with the least moves in the
queue, I decided to use a tuple with three int arguments, one for the row, one
for the column, and one for the number of moves it takes. With this, I pushed
the tuple onto the queue to indicate that the tupled square (start) had been visited. It then enters the for loop where I have the currentSquare pair to indicate
which square its currently on, which takes the front tuple of the queue and the
moves. Once currentSquare is equal to the end square (location is at the end),
the number of moves it took gets returned. The following lines are iterations of
undergoing all the moves with checks if it goes out of bounds, if the square was
visited, or if it was blocked. The time complexity of the BFS would be O(V +
E) (vertices + edges)
