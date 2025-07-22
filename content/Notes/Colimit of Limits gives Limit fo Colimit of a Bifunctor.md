---
tags:
  - Note
---
202506160106

Tags : [[Category Theory]]
# Colimit of Limits gives Limit fo Colimit of a Bifunctor
---
>[!theorem]
>Given a bifunctor $F:I \times J \to C$, so that the displayed limits and colimits exist, there is a canonical map:
>$$
>\kappa : \underset{i\in I}{\text{colim}} \lim_{j \in J} F(i, j) \to \lim_{j \in J}\underset{i\in I}{\text{colim}}\ F(i, j)
>$$

By [[Representable Universal Property of Colimits]] to define the above morphism, we need to define
$$
\Big(\lim_{j\in J} F(i, j) \xrightarrow{\kappa_{i}} \lim_{j \in J}\underset{i'\in I}{\text{colim}} F(i', j)\Big)_{i\in I}
$$
By [[Representable Universal Property of Limits]], each $\kappa_{i}$ is a map to a limit to it can be defined using
$$
\Big(\lim_{j' \in J}\ F(i, j')\xrightarrow{\kappa_{i,j}}\underset{i'\in I}{\text{colim}}\ F(i',j)\Big)
$$
Defining $\kappa_{i, j}$ is starightforwared:
$$
\kappa_{i, j} : \lim_{j'\in J}\ F(i, j') \xrightarrow{\pi_{i,j}} F(i, j)\xrightarrow{\iota_{i,j}} \underset{i'\in I}{\text{colim}}\ F(i', j) 
$$
Where $\pi_{i, j}$ is the leg of a limit cone and $\iota_{i, j}$ is the leg of a colimit cocone.


---
# References
- [[Representable Universal Property of Limits]]
- [[Representable Universal Property of Colimits]]
- [[Choosing Limits of diagrams in Functorial]]
- [[Filtered Colimits commute with finite limits in Set]]