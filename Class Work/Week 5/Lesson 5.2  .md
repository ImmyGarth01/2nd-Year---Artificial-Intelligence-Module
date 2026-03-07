# Lesson 5.2 - Video & Slides: #

### Informed Search 
Uses search strategy for sproblem-specific knowledge 
* The evaluation function is constructed as a cost estimate, so the node with the lowest evaluation is expanded first
* The choice of f determines the search strategy
* The component of f as a heuristic function is denoted h(n)
* h(n) = estiamted cost of the cheapest path from the state at node n to a goal state
* if n is a goal node, then h(n) = 0
  
#### Greedy Best-First Search: ####
Tries to expand the node that is closest to the goalonthe grounds that it is likely to lead to a solution 
* It evaluates nodes using the heurisitc function f(n) = h (n)
* The straight line distance heuristic is called h. SLD
* the node with the lowest h is expanded first
  
#### A* Search: ####
Evaluateds its nodes by combining g(n), the cost to reach the node and h(n), the cost to get from the node to the goal
* f(n) = g(n) + h(n)
Since g(n) gives the path cost from the start node to node n, and h(n) is the estimated cost of the cheapest path from n to the goals, we have:
* f(n) = estimated cost of the cheapest solution through n 
