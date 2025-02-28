---
tags:
  - Note
  - Incomplete
---
202502281902

Tags : [[Weighted Automata and Transducers]]
# Stochastic Languages are Regular if Threshold Point is Isolated
---
>[!theorem]
>Given a [[Probabilistic Automata]] $\cal P$ and a real number $k$ which is isolated with respect to $\mathcal P$, The [[Threshold Languages|threshold language]] $\mathcal P_{\bowtie k}$ is regular.

For any word $w$ we have a probability distribution $I \cdot \mu_{w}$.

So on the space of probability distributions on states, we partition and find myhill nerode classes there. Then we try to show that they are finite.

Let $\delta$ be the witness of $k$ being isolated, the radius of the ball around it that does not interesect with the image of $\cal P$.

Then we take the set and partition into (hyper)cubes of size $\frac{2\delta}{n}$. So the  distance ($P_{1}$ norm) between any 2 points in a cube is at most $2\delta$.

>[!todo] TODO draw diagram.

Now we show that if 2 words are not in the same myhill nerode class, they will be in different cubes. Let $u, v$ be 2 such words.

Then we have, WLOG, $I \cdot \mu_{uw} \cdot F > k + \delta$ and $I \cdot \mu_{vw} \cdot F < k - \delta$ for some $w$.
So we have $(I \cdot \mu_{u} - I \cdot \mu_{v})\cdot \mu_{w}\cdot F > 2\delta$

Then we simplify as follows:
$$
\begin{align}
(I \cdot \mu_{u} - I \cdot \mu_{v}) \cdot \mu_{w} \cdot F &> 2\delta \\
\sum_{i \in [1..n]} (a_{i}-b_{i})(\mu_{w} \cdot F)_{i} &> 2\delta
\end{align}
$$
Since each row of $\mu_{w}$ represent transition in a probabilistic automata, they all add up to $1$ and no entry of $F$ is more than $1$, so $(\mu_{w} \cdot F)_{i}$ is at most $1$.

We also have that 
$$
\begin{align}
\sum_{i\in [1..n]}(a_{i}-b_{i}) \cdot (\mu_{w} \cdot F)_{i} > 2d
\end{align}
$$
For only the terms where $a_{i}- b_{i}$ is positive.
Hence $\sum(a_{i}-b_{i})>2d$ for those terms which proves the theorem.

---
# References
