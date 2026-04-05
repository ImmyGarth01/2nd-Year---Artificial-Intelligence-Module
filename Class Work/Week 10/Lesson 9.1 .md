# Lesson 9.1 - Video & Slides: Forward Chaining #

## Expert System ##
- An expert system is a computer application that uses rules, approaches and facts to provide solutions to complex problems
- There are three components in an expert system: the user interface, inference engine, knowledge base
- The high valued knowledge is stored int he Knowledge base which is derived from human experts and knowledge engineers
- Forward chaining techniques are used to push the knowledge through the inferance engine and this is used to come up with strategies
- The user interface allows users to interact with the expert knowledge 
  
### Forward Chaining 
Forward chaining is a method of reasoning in AI in which inference rules are applied to existing data to extract additional data until an endpoint (goal) is achieved
- You use existing facts to come up with decisions and compare these descisions to each other to come up with the best one
- it is used in planning, monitoring, cotnrolling and interpreting applications

#### Forward Chaining - Properties
- The process uses a down-up apprach
- It starts from an initial state and used facts to make a conclusion
- The approach is data-driven
- It's employed in expert systems and production rule systems

#### Example 
A is the starting point, A -> B represents a fact. This fact is used to achieve a decision B 

Tom is running (A)
If a person is running, he will sweat (A -> B)
Therefore, Tom is sweating 

### Advantages of Forward Chaining 
- It can used to draw multiple conclusions
- It provides a good basis for arriving at conclusions
- It's more flexible than backward chaining because it does not have a limitation on the data derived from it

### Disadvantgaes of Forward Chaining 
- The process of forward chaining may be time-consuming. It may take a lot of time to eliminate and synchronize available data
- Unlike backward chaining, the explanation of the facts or observations aren't clear. the former uses a goal-driven methods that arrives at conclusions efficiently 
