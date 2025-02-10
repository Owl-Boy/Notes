---
tags:
  - Note
  - Incomplete
---
202502100202

Tags : [[Topics in Algorithms]]
# Fractional Tree Packing
---
>[!theorem]
>The size of the optimal *fractional tree packing* is given by:
>$$
>\tau_{\text{frac}}(G) = \min_{P} \frac{|E_{P}|}{|P|-1}
>$$

The proof for this theorem falls from an [[Primal - Dual LP]] algorithm.

Let $\mathcal T$ be the set of all spanning trees of $G$. Then our goal is to have as many trees as possible, which can be written as 
$$
\text{maximize:}\quad\sum_{t\in\cal T}y_{t}
$$
where $y_{T}$ is a variable for each tree. This is subject to the constraint that each edge is a part of at most 1 tree in total, so for each edge $e$ let $\mathcal T_{e}$ be the set of spanning trees that contain $e$.

$$
\begin{align}

\sum_{t\in \mathcal T_{e}}y_{t} \leq 1\;\;&, \forall e\in E \\
y_{t} \geq 0\;\;&,\forall t\in \mathcal T
\end{align}
$$

We find a solution by finding the solution of the dual of the LP.

$$
\begin{align}
\text{minimize}:\quad &\sum_{e\in E} x_{e} \quad \text{subject to}\\
\sum_{e\in t} x_{e \geq 1}\;\;&,\forall t\in \mathcal T \\
x_{e} \geq 0\;\;& ,\forall e\in E
\end{align}
$$
The dual can be though of as the fractional version of global min-cut. Both solutions exist because the problems have finite optima.

Now we use 2 claims
>[!lemma] Claim 1
>If in a optimal solution for the dual, for some edge $e$ we have $x_{e}=0$, then we can delete that edge from the graph and the problem will still have an optimal solution for tree packing of the same value.

Previous optimal solution works

>[!lemma] Claim 2
>If $x_{e}>0$ for all $e$, then consider the partition $P$ of singletons:
>$$
>\tau_{\text{frac}}(G) = \frac{|E|}{|V|-1}
>$$

Proof is by complementary slackness.

These 2 claims directly imply the theorem.

---
# References
