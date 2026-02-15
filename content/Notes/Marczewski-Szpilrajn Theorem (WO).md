---
id: Marczewski-Szpilrajn Theorem (WO)
aliases:
  - Marczewski-Szpilrajn Theorem
tags:
  - Note
---
202602151706

Tags : [[Model Theory]] [[Order Theory]]
# Marczewski-Szpilrajn Theorem
---
> [!THM] 
> Any partial order can be extended to a real order.

Consider a partial order $(X, \le)$. 

By [[Axiom of Choice and its Variants|Well Ordering Principle]], there is a well ordering $(X, \trianglelefteq)$.

Consider the set $S : X\to\mathbb B$, and the lexicographical ordering(relative to $\trianglelefteq$).

We also have $f : X\to S$ where $f(x)= y \mapsto x \le y$, we write these as $f_x$.

Note that the $f$ is an injection. if $f_x=f_y$ then $f_y(y) = 0 = f_x(y)$ thus $x\le y$ and by symmetry we get $y\le x$ and by asymmetry of $\le$ we get $x=y$.

Also note that $x\le y \Rightarrow f_x\le f_y$. Thus we lift the linear order on $S$ to a linear order on $X$. 

---
# References
- [[Axiom of Choice and its Variants]]
- [[Marczewski-Szpilrajn Theorem (Compactness)]]
