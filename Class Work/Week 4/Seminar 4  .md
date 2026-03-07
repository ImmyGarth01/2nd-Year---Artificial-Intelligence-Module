# Seminar 4 Questions 

## Definitions
##### State - This refers to the environment the agent is in, a world state is the real life state and a representational state is an fake one of the real world that an agent can use to decide future plans 
##### State Space - This is the graph where all of the states are, these are connected by actions that allow the agent to flow from one to another 
##### Search Tree - This is a tree graph which has a root node and a series of children nodes coming off of this 
##### Search Node  - A node in a search tree
##### Goal Action- An action that the agent can complete 

# Binary Search Tree
 For the set of keys (nodes) {1,4,5,10,16,17,21}, draw binary search trees of height 3,4,5,6.
       
         10
       /   \
      4     17                     H = 3
     / \    / \
    1   5  16 21

 
     

        10
       /   \
      4     17                     H = 4
     / \     \
    1   5    21
       /
       16




        10
       /  
      4                           H = 5
     / \    
    1   5  
         \
          17
          / \
        16   21




     1
      \
        4
         \                        H = 6
          5
           \
            10
              \
               16
                 \
                  17
                    \
                    21
