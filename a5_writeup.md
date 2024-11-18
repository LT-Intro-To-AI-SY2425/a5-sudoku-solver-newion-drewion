# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

DFS is definitly better for performance, given that it only has to store the current path and not every other possible path, which makes it more applicable for complicated puzzles. BFS might be more preferable, however, if the puzzle was one that required the "best" of multiple solutions, or if it was just a smaller puzzle alltogether. 

2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

DFS uses LIFO, meaning the push and pop determines whether to move deeper into the branch or to backtrack. BFS uses the FILO order, meaning every possibility is attempted before moving deeper. I couldn't get BFS to work, but DFS functioned well for our purposes. 

I didn't know of any alternatives to these two data structures, so I looked some up, and the one that caught my eye was "Deque (Double-Ended Queue)", which combines the idea of a stack and a queue, allowing elements to be added from both ends. 

3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?

The first thing that comes to mind is that BFS would become less practical, seeing as how brute-force methods get exponentially worse and worse as the number of permutations grows. (for example, a 16x16 or 25x25 sudoku). A good way to adapt the sudoku solver would be to (somehow) teach it some sudoku strategy, such as an "x-wing" or the "sudoku swordfish" which could speed up the solving process. 

This could be used in the real-world in robotics! I was thinking about how DFS and BFS are both commonly used for robots that follow black tape on tables (or any other kind of pathfinding "game") and try to navigate a course. I know that this also isn't super "real-world", seeing as how people don't particularly need robots that follow black lines, but it's a step in the right direction.