---
tags:
  - Note
  - Incomplete
---
202508072008

Tags : [[Manifolds]]
# Transition Functions
---
Consider the construction [[Unit Circle is a Manifold]].

Let $U_{1}$ (and $f_{1}$) and $U_{2}$ (and $f_{2}$) be the open sets that are used to describe the co-ordinate charts. We have the $f_{1}$ is defined on $S^1 \setminus \{(0,-1)\}$ and we have $f_{2}$ defined on $S^1 \setminus \{ (0,1) \}$. So if we restrict the function to intersection of $U_{1}$ and $U_{2}$ Then we can get a function
$$
\phi_{21}=f_{2} \circ f_{1}^{-1}:\mathbb{R} \setminus 0 \xrightarrow \sim \mathbb{R} \setminus 0
$$
which sends $x:\mathbb{R} \setminus 0$ to $\frac{1}{x}$.

The function $\phi_{21}$ is called a transition function.

More generally, suppose $X$ is any topological manifold and let
$$
\begin{align}
f_{1} &:U_{1} \to \tilde{U_{1}}\\
f_{2} &:U_{2} \to \tilde{U_{2}}
\end{align}
$$
>[!definition]
>Let $X$ be a [[Topological Manifold]], and let $(f_{1},U_{1})$ and $(f_{2},U_{2})$ be two coordinate charts on $X$. The transition function between two co-ordinate charts is the function 
>$$
>\phi_{21} =f_{2}\circ f_{1}^{-1} 
>$$


---
# References
- [[Unit Circle is a Manifold]]
- [[Topological Manifold]]