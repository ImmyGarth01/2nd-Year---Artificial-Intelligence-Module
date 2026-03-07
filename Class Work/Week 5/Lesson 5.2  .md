# Lesson 5.2 - Video & Slides: #

### Informed Search 
Uses search strategy for sproblem-specific knowledge 
* The evaluation function is constructed as a cost estimate, so the node with the lowest evaluation is expanded first
* The choice of f determines the search strategy
  
#### Greedy Best-First Search: ####
This refers to the strategies that have no additional information about states beyond what they have been provided in the problem definition 
All they can do is generate successors and distinguish a goal state from a non-goal state

#### Depth-First Search (DFS): ####
The strategy here is to expand the deepest node first

##### Example:

        S
