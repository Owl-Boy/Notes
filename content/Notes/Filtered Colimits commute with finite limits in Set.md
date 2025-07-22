---
tags:
  - Note
---
202506160206

Tags : [[Category Theory]]
# Filtered Colimits commute with finite limits in Set
---
>[!theorem]
>Given a filtered small category $J$ and a finite category $I$, given a bifunctor $F:I \times J \to \text{Set}$, we have a canoncial map 
>$$
>\kappa: \underset{j\in J}{\text{colim}} \lim_{i\in I}\ F(i, j) \to \lim_{i\in I} \underset{j\in J}{\text{colim}} F(i, j)
>$$

By [[Limits in the Category of Sets]], an element on the right side is a cone $\lambda$ with summit $1$ over $\underset{j\in J}{\text{colim}}\ F(-, j)$. Since $I$ if finite, this is given by a finite collection of cones $\lambda_{i} \in \underset{j\in J}{\text{colim}} F(i, j)$ satisfying a finite number of compatibility conditions.

Since $J$ is filtered, there is some sufficiently large $t\in J$ so that for each $i\in I$ the $\lambda_{i}$ are represented by the elements $\lambda'_{i}\in F(i, t)$ such that those elements assemble into a cone 
$$
\Big( 1 \xrightarrow{\lambda_{i}'}F(i, t)\Big)_{i\in I}
$$
This cone defines an element in $\lim_{I} F(-, t)$. Which is chooses an element from the left side which maps to it. making $\kappa$ surjective.

Given a pair of elements on the left side, represented as cones 
$$
\Big(1\xrightarrow{\alpha_{i}}F(i, j) \Big)_{i\in I}\quad\text{and}\quad \Big(1\xrightarrow{\beta_{i}}F(i, k) \Big)_{i\in I}
$$
If they have the same image under $\kappa$, then for each $i\in I$ there is some $t_{i}\in J$ for which $\alpha_{i}$ and $\beta_{i}$  have a common image in $F(i, t_{i})$. Since $I$ is finite and $J$ is filtered, there is some $t$, $\alpha_{i}$ and $\beta_{i}$ have a common in image in $F(i, t)$ for all $i$.

But that means $\alpha$ and $\beta$ are the same functions, making the two inputs same. Hence $\kappa$ is injective.

---
# References
- [[Filtered Category]]
- [[Limits in the Category of Sets]]
- [[Colimit of Limits gives Limit fo Colimit of a Bifunctor]]