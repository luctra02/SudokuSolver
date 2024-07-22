# CSP Solver for Sudoku

This project implements a general solver for Constraint Satisfaction Problems (CSPs) using backtracking search and the arc-consistency algorithm AC-3. The solver is used to solve Sudoku puzzles of varying difficulty.

## Features

- General CSP solver using backtracking and AC-3
- Sudoku solver capable of handling puzzles of varying difficulty
- Example implementation for the map coloring problem

## Requirements

- Python 3.x

## Usage

### Solving Sudoku

1. Prepare a Sudoku puzzle in a text file where empty cells are represented by '0'.
2. Use the `create_sudoku_csp(filename)` function to create a CSP instance.
3. Call the `backtracking_search()` method to solve the puzzle.
4. Print the solution using `print_sudoku_solution(solution)`.

```python
csp = create_sudoku_csp("easy.txt")
result = csp.backtracking_search()
if result:
    print_sudoku_solution(result)
else:
    print("No solution found")
```

## Example Output

### Easy

```python
backtrackCounter: 1
falseCounter: 0
7 8 4 | 9 3 2 | 1 5 6 
6 1 9 | 4 8 5 | 3 2 7 
2 3 5 | 1 7 6 | 4 8 9 
------+-------+------
5 7 8 | 2 6 1 | 9 3 4 
3 4 1 | 8 9 7 | 5 6 2 
9 2 6 | 5 4 3 | 8 7 1 
------+-------+------
4 5 3 | 7 2 9 | 6 1 8 
8 6 2 | 3 1 4 | 7 9 5 
1 9 7 | 6 5 8 | 2 4 3 

```


- **backtrackCounter**: 1
  - The backtracking algorithm was called 1 time.
- **falseCounter**: 0
  - The number of times the algorithm found that a partial assignment was invalid and had to backtrack was 0.


