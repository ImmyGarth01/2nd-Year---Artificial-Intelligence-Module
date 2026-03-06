# Lesson 3.2 - Video & Slides: #

## Structure of the Agent ##
Agent = architecture + program 
- The agent function is to work on mapping from percepts to actions
- The programm is assumed to run on a computing device with physical sensors and actuators (architecture)
- It is the architecture that makes the percepts from the sensors available to the actuators
- The agent will take the current/entire percept as input from the sensors and return an action to the actuators 
  
#### TABLE - DRIVEN - AGENT ####
- So this function is expected to return an action
- It starts with a percept and an empty table, as the percept sequence increases the table is populated with different actions it can take until there are no more percepts, then the table is looked up adn then an action is returned

##### Pseduo Code: Vacumn cleaner agent 

if status = Dirty then return Suck
else if location = A then return Right
else if location = B then return Left
