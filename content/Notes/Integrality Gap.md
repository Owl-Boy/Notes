---
tags:
  - Note
---
202501311501

Tags : [[Linear Programming]]
# Integrality Gap
---
For a given problem instance, there might be a difference in the optimal value that the LP for that problem gives us, and the optimal value that the *integral* LP gives. We define the highest (in a minimisation problem) such gap to be the integrality gap (as a ratio).
For an approximation algorithm, the best approximation ratio that we can get is bounded by this gap.

For example, in the [[Max Independent Set]] problem, given the complete graph as the instance, the $OPT(ILP)$ would be $1$, because we can have at most $1$ vertex in an independent set, while the $OPT(LP)$ would be $n$ by assigning all the vertices $\frac{1}{n}$. Here, the integrality gap is $\frac{1}{n}$, and thus we can't get a better approximation than $\frac{1}{n}$, an in fact, it is very difficult to find good approximation algorithms for max independent set instances.

$OPT(LP)\le OPT(ILP)\le$ our solution

**Integrality gap** $=\max_\limits{\text{all instances}}\frac{OPT(ILP)}{OPT(LP)}$
integrality gap $\le$ approximation ratio

---
# References
