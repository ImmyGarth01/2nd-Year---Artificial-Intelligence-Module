# Lesson 5.1 - Video & Slides: #

#### Uniformed Search: ####
This refers to the strategies that have no additional information about states beyond what they have been provided in the problem definition 
All they can do is generate successors and distinguish a goal state from a non-goal state

#### Depth-First Search (DFS): ####
The strategy here is to expand the deepest node first

##### Example:

        S
       / \
      B   H
     / \    \
    A   D    G

So assuming the intial state is S and the goal state is G the search would be:
{S,B,A,D,H,G}

##### Is It Complete? #####
m could be infititie so only if cycles are prevented 

##### Is It Optimal? #####
No, it finds the "leftmost" solution, regardless of depth or cost 





#### Breadth-First Search (BFS): ####
The strategy here is to expand the shallowest node first

##### Example:

        S
       / \
      B   H
     / \    \
    A   D    G

So assuming the intial state is S and the goal state is G the search would be:
{S,B,H,A,D,G}

##### Is It Complete? #####
D could be infititie so only if a solution exists yes 

##### Is It Optimal? #####
Only if all costs are 1 




#### Uniform Cost Search: ####
The strategy expands the cheapest node first 

##### Example:

           S (0)
          / \
     (3) B   H  (2)
     / \      \
    A   D      G  (1)

So assuming the intial state is S and the goal state is G the search would be:
{S,H,G}

##### Is It Complete? #####
Assuming the bes tsolution has a finite cost and minimum arc cost is positive then yes

##### Is It Optimal? #####
Yes
