# Lesson 11.1 - Video & Slides: Bayes Network #

## Why Use Bayes' Network instead of Probability Table?
There are a lot of entries to fill up the table when there are lots of random variables, this means that there needs to be fewer numbers 

### Independance 
- The variables A and B are independant from each other, meaning that the knowing the income of A does not inform you about the income of B
- It lets you focus and avoids complexity, one thing can link to a finite numbers of things instead of infinte probability 

### Example 
## Bayesian Network Example: Rain → Sprinkler → Wet Grass

### Variables
- R: Rain
- S: Sprinkler
- W: Wet Grass

### Structure (graph)
R → W ← S

### Independence assumption
Wet grass depends only on Rain and Sprinkler.

### Factorization
P(R, S, W) = P(R) * P(S) * P(W | R, S)

### Example probabilities
- P(R = 1) = 0.2
- P(S = 1) = 0.5

- P(W = 1 | R=1, S=1) = 0.99
- P(W = 1 | R=1, S=0) = 0.9
- P(W = 1 | R=0, S=1) = 0.8
- P(W = 1 | R=0, S=0) = 0.0

### What this model does
You can compute things like:
- P(W) (probability grass is wet)
- P(R | W) (probability it rained given wet grass)
