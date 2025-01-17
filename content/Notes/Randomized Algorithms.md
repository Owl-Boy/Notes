---
tags:
  - Note
  - Incomplete
---
202501172201

Tags : [[Algorithms]]
# Randomized Algorithms
---
A *Randomized Algorithm* is algorithm that employs a degree of randomness as a part of its logic or procedure. The point is to trade determinism or correctness in all runs with good performance.

A Randomized Algorithm generally falls into $2$ categories:
- **Las Vegas Algorithm**: Where the algorithm terminates with the correct answer always, but the running time is a random variable. And one would want a bound on the expected runtime, or on the runtime with high probability. ^1314ea
- **Monte Carlo Algorithm**: Here the runtime of the algorithm is determined, but the algorithm only gives the correct answer above some probability threshold. 

---
# References
[[Karger, Klein and Tarjan's Algorithm]]