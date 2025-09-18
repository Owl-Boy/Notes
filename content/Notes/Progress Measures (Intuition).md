---
tags:
  - Note
  - Incomplete
---
202509131809

Tags : [[Games on Graphs]]
# Progress Measures (Intuition)
---

Parity games are games where the winning condition depends on the entire infinite path (the winning condition checks if the vertices which occur infinitely many runs have maximum value of a particular parity). This makes constructions of finding strategy tedious (also kinda ugly). 

A **progress measure** is an attempt to capture the existence of a strategy of a parity game in a local property inspired by the following example:

>[!example]
>Consider a graph $G = \langle V_{o}\sqcup V_{e}, E\rangle$ which is the following cycle:
>$$
>G := v_{0} \to v_{1} \to v_{2} \cdots v_{n} \to v_{0}
>$$
>
>Here let the possible priorities assigned to vertices be $\{ 1, 2 \}$. To check if the loop is winning for the even player, we just need to make sure that its not an odd cycle, which is trivial in this case, but in general, we can assign to each $1$-priority vertex a number such that in any path, an our going edge from a $1$ vertex will go to a vertex whose assigned number is strictly smaller.
>Thus, if we have a degree 2 vertex here, we can assign it 0, and moving along the cycle backwards we assign numbers to it all 1 vertices in increasing order, if there are no 1 vertices then its not possible. 

We now generalize it for the cases when the priorities might have more numbers that $\{ 0,1,2 \}$ and hence assigning numbers would not be enough.

Thus we define progress measure which are precisely an ordered set which has the properties that we are interested in. 

Now consider the case when the maximum priority is $4$, so the possible priorities we are looking at are $\{ 1,2,3,4 \}$ we pay attention to the visits of vertices with degrees $1$ and $3$, so we will attack 2 numbers to each vertex, one to make sure that our max infinite degree is not $1$, and another to make sure that our max infinite degree is not $3$, we call those assignments $\xi_{1}$ and $\xi_{3}$ respectively, and we would not want our cycle to follow the following local property:
$$
\begin{matrix}
\text{if }p(v_{i}) =1 \text{ then } & \xi_{1}(v_{i})>\xi_{1}(v_{i+1})  & \xi_{3}(v_{i}) \geq \xi_{3}(v_{{i+1}}) \\
\text{if }p(v_{i}) =2 \text{ then } & \text{no restriction of }\xi_{1} & \xi_{3}(v_{i}) \geq \xi_{3}(v_{{i+1}}) \\
\text{if }p(v_{i}) =2 \text{ then } & \text{no restriction of }\xi_{1} & \xi_{3}(v_{i}) > \xi_{3}(v_{{i+1}}) \\
\text{if }p(v_{i}) =2 \text{ then } & \text{no restriction of }\xi_{1} \text{ or }\xi_{3}& \\
\end{matrix}
$$

This exact idea can be used to generalized the idea of progress measures to a graph with arbitrarily high max priority. This is fomalized in [[Parity Progress Measures on Graphs]].

---
# References
