---
tags:
  - Note
---
202510110010

Tags : [[Parameterized Algorithms]]
# Kernelization Algorithm for MAXSAT
---
>[!question]
>$\text{MAXSAT}$ asks if given a formula in CNF, is there an assignnment of the literals such that at least $k$ clauses are satisfied.

Let $\varphi$ be a CNF formula with $n$ variables and $m$ clauses. Let $\psi$ be an arbitrary assignment to the variables and $\lnot\psi$  be the opposite assignment. Observe that either $\psi$ or $\lnot\psi$ satisfies at least $\frac{m}{2}$ clauses. Thus, if $m \ge 2k$, then the answer is a yes-instance.

Let $G_{\varphi}$ be the variable-clause incidence matrix. This is a bipartite graph with partitions $(X, Y)$ where $X$ is the set of variables in $\varphi$ and $Y$ is the set of clauses. There is an edge from $x$ to $y$ if either the clause $x$ is in $y$ or the clause $\lnot x$ is in $y$.

If there is a matching of $X$ into $Y$ then there is a truth assignment satisfying at least $|X|$ clauses. Thus in that case, $|X| \geq k$ would give a yes instance, otherwise $k>|X|$ and we get our desired clause.

Now, let $\varphi$ have at least $k$ variables. Using [[Hall's Marriage Problem|Hall's Theorem]] and [[Hopcroft-Karp Algorithm]] we can either find a polytime matching of $X$ into $Y$ or an inclusion minimal subset $C \subseteq X$ such that $|N(C)| <|C|$. If we found a matching then we get a yes-instance. Otherwise, we have a $C$. Let $H=N(C)$ and let $R$ be the rest of the graph. Select an arbitrarty $x\in C$, there will be a matching of $C-x$ into $H$ since $|N(C')| \geq |C'|$. We satisfy all the clauses in $H$. We have that in every assignment, we an make sure that $H$ is satisfied by manipulating the assingment of variables of $C$. Thus we have a simple reduction.

---
# References
[[Hall's Marriage Problem]]
[[Hopcroft-Karp Algorithm]]
[[Crown Decomposition]]
