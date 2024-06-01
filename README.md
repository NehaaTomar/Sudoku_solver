# Hey! I am Neha Tomar

# Introduction 
A Very Fast Sudoku Solver made in C++
This Sudoku solver is designed to solve Sudoku puzzles of any difficulty level. Sudoku is a popular logic-based number placement puzzle game. The objective is to fill a 9×9 grid with digits so that each column, each row, and each of the nine 3×3 subgrids that compose the grid (also called "boxes", "blocks", or "regions") contain all of the digits from 1 to 9 without repetition.

# Features
Solves Sudoku puzzles of any difficulty level.
Uses backtracking algorithm to efficiently find solutions.
Provides clear and easy-to-understand output.

# How to Use?
1. Clone this repository to your local machine.
   ''' bash
    git clone: https://github.com/NehaaTomar/Sudk_solver.git
   '''
3. Ensure you have a C++ compiler installed (e.g., g++).
4. Open a terminal or command prompt and navigate to the directory where you cloned the repository.
5. Compile the sudoku_solver.cpp file using the C++ compiler
   ''' bash
   g++ -o sudoku_solver sudoku_solver.cpp
   '''
7. Run the compiled program
   ''' bash
   ./Sudoku_solver
   '''
9. Input the Sudoku puzzle as a 9x9 grid, using '0' or '.' to represent empty cells.
10. The program will solve the puzzle and display the solution.

# How to Run ?
- # Compiling
    - Standard: g++ solver.cpp -o solver.exe
    - Faster: g++ -O3 solver.cpp -o solver.exe
    - Fastest(not recommended): g++ -Ofast solver.cpp -o solver.exe
  
- # Running
  - Put your sudoku puzzle in puzzle.txt, use numbers to represent given data and 0(Zero) to represent missing data with spaces in between every number.
  - Also put the size of the sudoku on the first line(look at examples in /puzzles)
  - Execute ./solver.exe in the terminal while in the root directory of the project.


# How did I achieve this speed ?
- To achieve this performance Donalds Knuths Algorithm X was used.
- The data structure used to implement Algo X is Dancing Links also proposed by Donald Knuth.
- I made a significant improvement in performance building the Toroidal Doubly Linked List to represent the puzzle as an exact cover problem. Time Complexity: O(n^3)
- And then the standard backtracking algorithm as described by Algorithm X.

## Usage/Examples

```
Here's an example of how to input a Sudoku puzzle:
Enter the Sudoku puzzle (use '0' or '.' for empty cells):
5 3 0 | 0 7 0 | 0 0 0
6 0 0 | 1 9 5 | 0 0 0
0 9 8 | 0 0 0 | 0 6 0
------+-------+------
8 0 0 | 0 6 0 | 0 0 3
4 0 0 | 8 0 3 | 0 0 1
7 0 0 | 0 2 0 | 0 0 6
------+-------+------
0 6 0 | 0 0 0 | 2 8 0
0 0 0 | 4 1 9 | 0 0 5
0 0 0 | 0 8 0 | 0 7 9

- # After solving, the output will be:
Sudoku puzzle solved:

5 3 4 | 6 7 8 | 9 1 2
6 7 2 | 1 9 5 | 3 4 8
1 9 8 | 3 4 2 | 5 6 7
------+-------+------
8 5 9 | 7 6 1 | 4 2 3
4 2 6 | 8 5 3 | 7 9 1
7 1 3 | 9 2 4 | 8 5 6
------+-------+------
9 6 1 | 5 3 7 | 2 8 4
2 8 7 | 4 1 9 | 6 3 5
3 4 5 | 2 8 6 | 1 7 9


```



