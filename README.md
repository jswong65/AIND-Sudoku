# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Naked twins is another approach (except eliminate and only_choice ) that can be used to eliminate the impossible solution. When two identical pair of values appear in two boxes within the same unit (row_unit, column_unit or square_unit), meaning these values can only be the solution of the two boxes, and cannot be the solutions of the other boxes. For example, if box A1 and B1 have the possible solution 12, which means the answer 1 and 2 can only be assigned to either A1 or B1. If other boxes in row 1 also have 1 or 2 as the potential solution, then both values should be excluded. By utilizing naked twins approach, we are able to eliminate the impossible solution, which can efficiently reduce the search space. 

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: In order to solve the Diagonal Sudoku, we can add two new units which includes boxes located on the two main diagonals. Therefore, there are four lists of units now in unitlist (row_units, column_units, square_units, and diag_units) which has 9+9+9+2 units (constraints) in total. The additional constraints can then be automatically applied to three functions (eliminate, only_choice, and naked_twins) for minimizing the possible values in a box. With those approaches (constraint propagation), the search space can be significantly reduced.  

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.