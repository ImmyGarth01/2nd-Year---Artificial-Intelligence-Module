# Lesson 7.1 - Video & Slides: Defining CSP #

## Constraint Satisfaction Problem (CPS) ##
- They describe a way to solve a variety of problems sufficiently
- It uses a factored representation for each state which is a set of variables in which each has a value
- A problem is then solved when each variable has a value that satisfies all the constraints of the variable 
- CSP search algorithms take a advantage of the strucuture of states and use general purpose rather than specific problem heuristic to enable a solution to a complex problem
- The main idea is to eliminate large sections of the search spaces by identifying variable value combinations that violates all constraints
  
### Components of CSP ###
- X = the seat of variables {x1,...,xn}
- D = set of domains {d1,...,dn}, one for each variable, this is paired with each variable having a set of allowable values for that variable
- C = the set of constraints that specify allowable combinations of the values #

#### Australian Map example ####
- X = The territories
- D = The colours
- C = adjacent regions must have different colours

#### Graphs ####
The Australian map is an example of a Binary CSP as each constraint relates to two variables 


Constraint Graph = Where nodes are variables and arc are constraints 


### Types of Constraints 
- Unary contraints = involve a single variable (ex - a specific region can't be green)
- Binary constraints = involve a pair of variables (ex - One region can't be the same colour as another specific region)
- Higher-order constraints = involve 3 or more variables (ex - cryptarithemtic column constraints)
