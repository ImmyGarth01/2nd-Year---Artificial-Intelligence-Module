# Seminar 5 Questions 

## Using Search Trees to explain DFS and BFS

### Question 1 – Search Tree, DFS and BFS

The graph contains:

- **Start node:** S  
- **Goal node:** G  

Nodes include:  
`S, a, b, c, d, e, f, g, h, p, q, r`

---

# Search Tree (from S)

A simplified search tree generated from the start node:

```
S
├── d
│   ├── b
│   │   └── a
│   │       └── c
│   │           └── e
│   │               ├── f
│   │               │   └── G
│   │               └── h
│   │                   └── r
│   └── e
│
└── p
    └── q
        └── h
            └── e
```

Note:  
This is a **search tree**, not the original graph.  
If the graph contains multiple paths to the same node, the search tree may repeat nodes.

---

# Breadth First Search (BFS)

## Definition

Breadth First Search explores nodes **level by level**, starting from the root node.

It expands all nodes at one depth before moving to the next level.

---

## Data Structure

Queue (**FIFO – First In First Out**)

---

## BFS Traversal Example

```
Level 0
S

Level 1
d, p

Level 2
b, e, q

Level 3
a, h

Level 4
c, r

Level 5
f

Level 6
G
```

---

## BFS Characteristics

| Property | Description |
|----------|-------------|
| Completeness | Yes (if branching factor is finite) |
| Optimality | Yes (if all step costs are equal) |
| Data Structure | Queue |
| Memory Usage | High |

---

# Depth First Search (DFS)

## Definition

Depth First Search explores **as far as possible along a branch before backtracking**.

---

## Data Structure

Stack (**LIFO – Last In First Out**) or recursion.

---

## DFS Traversal Example

One possible DFS traversal:

```
S → d → b → a → c → e → f → G
```

The search stops when the goal node is found.

---

## DFS Characteristics

| Property | Description |
|----------|-------------|
| Completeness | No (may get stuck exploring deep paths) |
| Optimality | No |
| Data Structure | Stack |
| Memory Usage | Low |

---

# Question 2 – A* Algorithm

Find the **most cost-effective path from A to G using the A* algorithm.**

---

# Heuristic Values h(n)

| Node | h(n) |
|------|------|
| A | 11 |
| B | 6 |
| C | 99 |
| E | 7 |
| D | 1 |
| G | 0 |

---

# Edge Costs

| Edge | Cost |
|------|------|
| A → B | 2 |
| A → E | 3 |
| B → C | 1 |
| B → G | 9 |
| E → D | 6 |
| D → G | 1 |

---

# A* Formula

```
f(n) = g(n) + h(n)
```

Where:

- **g(n)** = cost from start node to node n  
- **h(n)** = heuristic estimate from node n to the goal  
- **f(n)** = estimated total cost of the path

---

# Step-by-Step Solution

## Step 1 – Start at A

```
g(A) = 0
h(A) = 11
f(A) = 11
```

Expand node **A**.

---

## Step 2 – Expand neighbours of A

### Node B

```
g(B) = 2
h(B) = 6
f(B) = 8
```

### Node E

```
g(E) = 3
h(E) = 7
f(E) = 10
```

Choose node **B** because it has the smallest f value.

---

## Step 3 – Expand B

### Node C

```
g(C) = 3
h(C) = 99
f(C) = 102
```

### Node G

```
g(G) = 11
h(G) = 0
f(G) = 11
```

Open list now:

```
E (10)
G (11)
C (102)
```

Choose **E**.

---

## Step 4 – Expand E

### Node D

```
g(D) = 9
h(D) = 1
f(D) = 10
```

Choose **D**.

---

## Step 5 – Expand D

### Node G

```
g(G) = 10
h(G) = 0
f(G) = 10
```

Goal node reached.

---

# Optimal Path

```
A → E → D → G
```

---

# Total Cost

```
A → E = 3
E → D = 6
D → G = 1

Total Cost = 10
```

---

# Question 3 – Two Friends Meeting Problem

Two friends start in different cities and want to meet as quickly as possible.

Rules:

- Both friends move simultaneously.
- Each friend moves to a neighbouring city.
- Travel time between cities equals the road distance.
- The friend who arrives first waits for the other.

---

# (a) Search Problem Formulation

## State Space

A state is represented as:

```
(friend1_city, friend2_city)
```

Example:

```
(Arad, Bucharest)
```

---

## Initial State

```
(cityA, cityB)
```

Where each friend starts in a different city.

---

## Successor Function

Each friend moves to one neighbouring city.

Example transition:

```
(Arad, Sibiu) → (Sibiu, Fagaras)
```

Both moves happen at the same time.

---

## Goal State

Both friends are in the **same city**.

```
(city, city)
```

Example:

```
(Bucharest, Bucharest)
```

---

## Cost Function

The cost of each step is:

```
max(d(i,j), d(k,l))
```

Where:

- d(i,j) = distance travelled by friend 1  
- d(k,l) = distance travelled by friend 2  

The friend that arrives earlier waits for the other.

---

# (b) Admissible Heuristics

Let:

```
D(i,j)
```

be the straight-line distance between cities.

---

### (i) D(i,j)

Admissible.

Reason:  
Straight-line distance never overestimates the real travel cost.

---

### (ii) 2 × D(i,j)

Not admissible.

Reason:  
Multiplying by 2 may overestimate the true cost.

---

### (iii) D(i,j) / 2

Admissible.

Reason:  
This value is always less than or equal to the true distance.

---

# (c) Are There Completely Connected Maps With No Solution?

No.

If the map is completely connected, every city is reachable from every other city.  
Therefore both friends can always meet in some city.

---

# (d) Are There Maps Where a Friend Must Visit the Same City Twice?

Yes.

This can happen when the road network forces a friend to backtrack.

Examples include:

- Dead-end roads
- Tree-like road networks
- Limited connections between areas

In these cases, the optimal path may require revisiting a city.

---

# Summary

| Topic | Key Idea |
|------|----------|
| BFS | Explores nodes level by level using a queue |
| DFS | Explores nodes deeply using a stack |
| A* | Uses f(n) = g(n) + h(n) to find optimal path |
| Meeting Problem | State representation is (city1, city2) |
| Admissible Heuristic | Must never overestimate the real cost |
