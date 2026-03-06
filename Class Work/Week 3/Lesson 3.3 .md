# Lesson 3.3 - Video & Slides: #

## Types of Agent ##
The different types of agent include:
* Simple relex agents
* Model-based reflec agents
* Goal-based agent
* Utility-based agents

### 1. Simple reflex agent
This is the simplest kind of agent. It selects actions on the basis of the current percept, ignoring the rest of the percept history 

### 2. Model-based reflex agent
This is the best way to handle partial observable, the agent will maintain an internal state based on the percept hisotry and therefore will represent some of the unobserved characteristics of states
- an agent will have a model of how the world behaves independantly from the agent and will be influenced by this
- It uses conditoin-action rules: such as if the world is DIRTY > THEN > CLEAN

  ### 3. Goal-based agents
  This agent needs a current state description as well as a goal in mind to work towards, this can be combined with a model to choose actions that work towards said goal
* The goal of a goal-based agent can be changed just by specifying another goal 
   ##### Structure: #####
  Percepts → Update state
State + Goal → Search / Planning
Best action → Execute


  ### 4. Utility-based agent
  An agents' utility function is an internalisatin of the performance measures.
  It chooses the actions that maxamises the expected utility action outcomes , the utility the agent expected to derive on average given the probability and unit of the ejection, so basically it works on the best otucome not just reaching the goal 
  
