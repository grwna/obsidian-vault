Joint probability distribution is expensive ($2^n$, where $n$ are unique variables). Bayesian Network **exploits independence**.

Structure:
- Nodes (variables)
- Directed arc (relationship between variables)
- Numerical parameters 

Bayesian network still requires $2^n$ nodes, but it is cheaper with nodes than raw probability like JPD.

Each node will have the probability of the parent, lets say:
```
A --> B -- > C
      ^
      |
      D
```

Then C will need P(c|b) and P(c|$\neg$b). B requires both the normal and the negation of both parents.

# Bayesian Network as Joint Probability Distribution
PPT Page 13, what if you want to calculate probability of some variabels (not all). For the variables not counted, calcualate ALL combinations of the probability   z1