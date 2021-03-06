# d-star-lite

This poject is based on the original [D* Lite paper](http://idm-lab.org/bib/abstracts/papers/aaai02b.pdf) by Sven Koenig and Maxim Likhachev.

The D* Lite algorithm was written to be a "novel fast replanning method for robot navigation in unknown terrain". It searches "from the goal vertex towards the current vertex of the robot, uses heuristics to focus the search" and efficiently uses the priortity queue to minimize reordering.

### Use of the project
Currently written for Python 3 and the biggest requirement is having Pygame. Instructions for installing pygame can be found at [https://www.pygame.org/wiki/GettingStarted](https://www.pygame.org/wiki/GettingStarted).

**PIP install:**
```pip install pygame```

This repo is used for the study and of path planning in real time in **GOOGLE's UAS air space system** 

Run the example demo with ```python3 main.py``` (or ```python main.py``` if you have Python 3 installed as such on your system or in your environment). The demo shows off the dynamic replanning ability of the path planning algorithm by allowing the user to add obstacles by clicking on cells in the grid. Our mobile agent is the red circle, while the goal cell is green. The agent has a visibility range, shown by the thin black lines, and added obstacles are not taken into account by the agent until they are visible and change to darker grey. Pressing space bar makes the agent observe new obstacles, replan if necessary, and advances on the current best path until the goal is reached.
