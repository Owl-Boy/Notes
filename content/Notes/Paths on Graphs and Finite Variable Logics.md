---
tags:
  - Note
---
202504291804

Tags : [[Finite Model Theory]]
# Paths on Graphs and Finite Variable Logics
---
In $\text{FO}$ one can write a formula $P_{n}(x, y)$ which is true if there is an at most $n$ length path between $x$ and $y$.

The statement about there being an arbitrary path can be expressed in stronger extensions of $\text{FO}$, for example 
- in $\mathcal{L}_{\infty, \omega}$, one can take the infinite disjunction of paths of all lengths. 
	- $\bigvee_{i\in \mathbb{N}} \varphi_{i}$
- In Fixed point logics, one can take the the transitive closure
	- $\varphi_{1}(x, y) \equiv E(x, y)$
	- $\varphi_{n+1} = \exists z_{n}, E(x, z_{n}) \land \varphi_{n}(z_{N}, y)$

These definitions use the entire power of $\mathcal{L}_{\infty, \omega}$ and hence are not nice, the logic is too strong to be wieldy, but the following can be done to the fixed point definition of the logic.

- $\varphi_{1}(x, y) \equiv E(x, y)$
- $\varphi_{n+1} \equiv \exists z \Big( E(x, y) \land \exists x(z=x \land \varphi_{n}(x, y))\Big)$

The same ideas can be used to describe transitive closures and fixed points, where one can carefully reuse variables, along with that one needs to be able to use infinitely many variables to get the entire power of $\mathcal{L}_{\infty, \omega}$. This indicates that restricting the given logic to have only finitely many variables is potentially of interest.

---
# References
