Hello, thanks for your interest in my code!

This goal of this project was to create a pacman agent that could efficiently
find the best path possible in a pacman game. The project itself was created
by a university course instructor, but the search algorithms and heuristic
functions were created by me. These can be viewed in search.py and
searchAgents.py.

To run the program, I use python in the command line. A valid example is:
```
py pacman.py -l mediumCorners -p SearchAgent -a fn=dfs, prob=CornersProblem
py pacman.py -l mediumCorners -p SearchAgent -a fn=bfs, prob=CornersProblem
py pacman.py -l mediumCorners -p SearchAgent -a fn=ucs, prob=CornersProblem
py pacman.py -l mediumCorners -p AStarCornersAgent
py pacman.py -l mediumCorners -p AStarFoodSearchAgent
py pacman.py -l bigSearch -p AStarFoodSearchAgent -z .5
```
These will run different layouts of the pacman arena and different problems, based
on the inputted arguments. The corners problem challenges a pacman to collect food
pellets from each of the four corners. The food search problem challenges a pacman
to collect all food in the arena in an efficient manner.

The most challenging aspect of this project was creating an admissible heuristic.
The heuristic I chose for the A* search agent uses the manhattan distance from
pacman to the closest food, plus the manhattan distance from that food to its
closest food, etc.
