# Seminar 3 Questions 

## Definitions
##### Agent - An entity that has sensors allowing them to recieve percepts and have actuators to make actions
##### Agent Function - A function that shows the agent's action based on every percept sequence 
##### Agent Program - The program that implements the agent function 
##### Rationality- When actions are chosen to maxmaise expected utility given the percepts up till that point 
##### Autonomy - When an agent's nehaviour and actions is determined by its own experience rather than just its coding 
##### Reflex Agent - An agent whose action depends on the current state/percept
##### Model-Based Agent - An agent whose action depends on an internal model of the current world state, this updated as time moves on
##### Goal-Based Agent - An agent whose action depends on what will achieve explicitly represented goals 
##### Utility Agent - An agent whose action depends on what it believes will maximize the expected utilty of the outcome state
##### Learning Agent - An agent whose behaviour improves ovewr time based on its experience 

## True or False? 

##### a) An agent that senses only partial information about the state cannot be perfectly rational.
False - Rationality refers to making the best decisions with the available information
##### b) There exist task environments in which no pure reflex agent can behave rationally.
True - A pure reflex agent disregards the past so cant make fully rational decisions 
##### c) There exists a task environment in which every agent is rational.
True 
##### d) It is possible for a given agent to be perfectly rational in two distinct task environments.
True
##### e) Every agent is rational in an unobservable environment.
False 
##### f) A perfectly rational poker-playing agent never loses
False 

### 3. Consider a modified version of the vacuum environment, in which the geography of the environment— its extent, boundaries, and obstacles— is unknown, as is the initial dirt configuration.(The agent can go Up and Down as well as Left and Right.)
a) Can a simple reflex agent be perfectly rational for this environment? Explain
No it cant it can't remember it's past meaning that it will get stuck when it tries to move 
b) Can a simple reflex agent with a randomized agent function outperform a simple reflex agent?
Design such an agent and measure its performance on several environments.
(defun ransomized-reflec-vacuum-agent (percept)
(destructing-bind (location status) percept
(cond ((eq status 'Dirty) 'suck)
(t (random-element ' (Left Right Up Down))))))

c) Can you design an environment in which your randomized agent will perform poorly?
