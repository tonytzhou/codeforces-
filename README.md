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
took O(n) time. <br>

**Diagon Alley** - For this problem, I took a straightforward approach using a greedy algorithm.
First, I gathered all the necessary inputs: money, number of items, prices, etc.
After collecting the inputs, I sorted the vector in ascending order and iterated
through it. For each iteration, I subtracted the price of the item and incremented
the number of items bought until the total amount of money was less than the
price of the item at index i. After that, I returned the total number of items
bought. The runtime of this algorithm is O(n log n) due to the sorting function
being called. <br>

**Merge the Candies** For this problem, I originally thought to implement a Huffman tree as it fits the
problem to keep adding the smallest number in order to get the most optimal solution. I then realized that I can use a priority queue to automatically sort itself,
keeping the minimum value at the front. To do this, I took the numbers inputted
and pushed it into the priority queue, then taking the first two values, popping
them, adding them together, and pushing whatever I got back into the priority
queue. This continued as long as there were numbers in the priority queue to
account for all the values. Lastly, I multiplied the end result by 2 to account
for Yihan counting the number she got twice every time, making it less redundant. <br>

**Simplest Knapsack in the World** For this problem, I knew that I had to use a dynamic programming approach
after going through it in class so much. I decided to use a pair to represent my data as I knew that the values and weights corresponded with one
another. I implemented dynamic programming through the function called
callDP taking in all the inputs I needed, along with the vector of a vector
to store all known values, being my “table”. The function first checks base
cases, being no items or no weightBudget, the proceeds to check if the value
at the vector is -1 or not. Best is then calculated recursively, taking the max
value I can get at a given weight, and then stored into dpVec <br>

**Longest Decreasing Subsequence** For this problem, I knew that it was extremely similar to the Longest Increasing
Subsequence DP problem, so I used that as a sort of framework. The nested
for loop calculates the LES at each position i from going through each element
in the subsequence from the second element and the inner loop checks if all
previous elements are greater than the current element i. Once this is checked
and valid, it gets pushed into the DP vector and keeps track of the max values.
By using max element at the end, I’m able to find the length of the longest
decreasing subsequnece. It would have a runtime of O(n^2) due to the double for loop. <br>

**Weighted Edit Distance** For this problem, we went over it in class so I had a rough idea of how to solve it
while utilizing the slides. I decided to call it in a separate function to not clutter
the main code, but first it initizliaes the 2d vector of dpVec in order to store the
minimum cost it would take to find the shortest edit distance. From then on,
the base cases are initialized, being the deletion cost and insertion costs. This is
shown through the deleting of i elements and the insertion of j elements. After
that the nested for loop is called, iterating all the prefixes of aSequence and
bSequence in order to calculate the minimum cost to transform the sequences.
Once it goes through all the insertion, deletion, and edit costs, then it takes the
minmum of them and updates the dpVec. Once all this is done, the min result
is returned at the end. Due to the double for loop as well, it would lead to
O(n^2) runtime. <br>


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

**Merge Them** - For this problem, I knew that I had to implement merge sort first and find a
way to keep track of the number of candies that Yihan has to prepare. I decided to do this with two functions: mergeSortCandyCounter, which initializes
the candies, and mergeTotalCandyCounter, which returns an integer that gets
added to the total candy count. mergeSortCandyCounter is primarily used to
call mergeTotalCandyCounter, keep track of the candies, and manage the array
being sorted, while mergeTotalCandyCounter performs the actual sorting.
In the main function, we take in the vector and output the result. The
runtime of the algorithm should be O(n log n), as this is the typical runtime of
merge sort <br>

**Patronus Charm** This problem is similar to the previous one with the longest decreasing subsequence. Instead of storing the length, we instead want to store the sum of the longest subsequence. The main first takes in the input from the array and then calls the dpFunction which initializes dpVector to go through and find the greatest sum. This is done through a nested for loop that takes the integer at the current sum of the longest increasing subsequence and the current one, then  taking the max of them. After going through all the loops, at the end it returns the greatest possible value. This is done in O(n^2) runtime due to the double for loop being present. <br>

**Selling Candies** For this problem, I knew that I had to implement Dijikstra’s algorithm with an
extra variable, being the cost that I could sell at each city. I decided to do this by
using a priority queue and comparing all the costs, distances, and max profits to
another. First, I use a vertex to label all the node that have a connecting edge, if
they don’t then it would be filled with 999999. The priority queue is then made
and the first point 0,0 is pushed onto it. While the priority queue is not empty,
it takes the current distance and current node and compares it to the neighbors
of current current node. If the distance to a neighbor is shorter than the current distance, then it updates it and calculates the profit at the end. This is
done through taking the sale price at a given node, (prices.at(i)), then subtracting it by how much it takes to get there times 2, representing going back and
forth from the nodes. This would result in a O(E log V) runtime due to having
to visit every node once, and uses a priority queue which has O (log V) runtime. <br>


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
