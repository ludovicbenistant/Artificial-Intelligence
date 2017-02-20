# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?
The goal of constraint propagation is to extract the maximum information out of our constraints. Here, our constraint propagation algorithm was already composed of two functions (elimination and only choice), but we add a third one called naked twins that can further reduce the search space and therefore speed up the solving process. 

Our naked twins function can remove values in a box given local knowledge. If two units have the same two possibility {'A1': '12', ‘A2':'12', …} then we know that 1 and 2 must be in one of these two boxes and not somewhere else. Therefore we can eliminate 1 and 2 from all other boxes in the row A.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?
Solving the diagonal sudoku was very similar than solving the basic Sudoku as we use the same functions. What has changed is the set of constraints we tell our algorithm to follow in the beginning. Now, not only we have constraints in term of lines, rows, and squares, but also in diagonal. 

Constraint propagation enables us to reduce the search space by gathering all the constraints that need to be fulfilled together. As each local constraint introduces further constraints for the rest of the board, we can narrow the probability of many boxes. 

Constraint propagation is mainly implemented by the combination of the function (also called strategy) elimination and only choice. Then we use the function search to complete the board. 


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

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in function.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.
