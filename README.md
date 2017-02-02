# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Constraint in the naked twins problem is that if there is a twin(two digit no) that occurs twice in a unit, then those digits can't occur anywhere else in the unit. So, for all units, we find if such a naked twin occurs, and then remove those digits from possible values of other boxes of the unit. To propgate this contraint, we apply it repeatedly, along with eliminate and only_once steps. So, eliminate -> only_once -> naked_twins -> eliminate -> only_once -> naked_twins, repeatedly we apply the three steps, in search of solution.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: In the Diagonal Sudoku problem, we have the added constraint, that all nine digits, can occur only once across the two diagonals. To take care of this constraint, I added the two diagonal units in the unitlist list of all units. Thus, when we apply the constraint propagation steps of "eliminate, only_once, naked_twins" over all the units, the diagonal constraint is taken care of since diagonal unit is a part of unitlist.

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