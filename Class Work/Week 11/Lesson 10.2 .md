# Lesson 10.2 - Video & Slides: Probabilistic Inference #

##### Probabilistic Inference 
Used to compute a desired probability from other known probabilities like calculating conditional probability from joint probability 

### The Product Rule
- Sometimes have conditional distributions but want the join
- The probability of both events = (probability of one event) × (probability of the other given the first)

### The Chain Rule
- We can write any joint distributions as an incremental product of conditional distributions
- A repeated application of the product rule to more than two variables.

### The Bayes' Rule
- There are two ways to factor a joint distributions over two variables in dividing
- The idea that we should update probabilities when you get new evidence.

## Bayes' Example
### 🔹 Example

Suppose:

- 1% of people have a disease → \( P(D) = 0.01 \)

- Test is 99% accurate:
  - \( P(+ \mid D) = 0.99 \)
  - \( P(+ \mid \neg D) = 0.01 \)

If you test positive, what’s \( P(D \mid +) \)?

\[
P(D \mid +) = \frac{0.99 \times 0.01}{P(+)}
\]

Compute \( P(+) \):

\[
P(+) = 0.99 \cdot 0.01 + 0.01 \cdot 0.99 = 0.0198
\]

So:

\[
P(D \mid +) = \frac{0.0099}{0.0198} = 0.5
\]

👉 Even with a good test, the probability is only **50%** because the disease is rare.
