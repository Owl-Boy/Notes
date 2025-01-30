---
tags:
  - Note
---
202403081403

Tags : [[Combinatorial Optimisation]], [[Topics in Algorithms]]
# Matroids (Whitney 1935)
---
A *Matroid* is a structure that generalized the notion of independent sets in vector spaces, and is heavily used in both linear algebra and graph theory.

>[!definition]
>A matroid $M$ has a ground set $E$, a collection $I$ of subsets of $E$, called independent sets, i.e. $M=(I,E)$ s.t.
>1. *Downward closure:* If $Y\in I$, then $\forall X\subseteq Y, X \in Y$.
>2. *Extension:* If $X,Y\in I, |X|<|Y|$ then $\exists e\in Y\setminus X$ s.t. $X\cup \{ e \}\in I$.

Matroids can also be used to capture partially finding a solution, in that scenario, the 2 constraints can be interpreted as.
- *Downward closure*: A part of a partial solution is a partial solution
- *Extension*: If $X$ is a smaller partial solution than $Y$, then it can be extended using something from $Y$.

>[!question]
>The extension property seems too strong? What makes sense for the greedy algorithm case to me is that it should be okay if for every $X$ there is some $Y$ for which the above condition holds.... hmm.

---
# References
