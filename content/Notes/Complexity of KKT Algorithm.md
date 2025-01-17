---
tags:
  - Note
---
202501172201

Tags : [[Topics in Algorithms]]
# Complexity of KKT Algorithm
---
The time complexity of the algorithm is $O(|E|)$ randomized, It always gives the correct answer, but its running time is a random variable with the expected runtime be bounded by $O(|E|)$.

- Step $1$ of the algorithm takes $O(|E|)$ time, it goes over all edges at most 6 times.
- Step 2 takes time $O(|E'|)$
- Step 4 uses [[Komlos's Algorithm]] which is in $O(|E'|)$
- Step 6 is constant time
- Step 3 and 5 are recursive call and computing their complexity is not trivial and will be done now.

Let $|V| = n$ and $|E| = m$. We define $|E_{1}|=m_{1}=\frac{m'}{2}$ and $|E_{2}|=m_{2}$.
We also define $|V'| = n' = \frac{n}{8}$ and $|E'| = m'$. 

>[!note]
>This definition of $|V'|$ uses the fact that Boruvka is run 3 times, if one wants to change that, then they must adjust other parameters, like probability threshold for step 2.

Also define $T(G)$ to be the time it takes to execute $\text{KKT}(G)$. Similarly, define $T_{m, n}$ to be the maximum  time taken by $\text{KKT}$ on any $m$-edge and $n$-vertex graph. 

$$
\begin{align}
T_{m, n} &= E [\![T_{m_{1}, n'}]\!] + E[\![T_{m_{2}, n'}]\!] + c(m + n) \\
&\text{assume : } T_{m, n} \leq 2c(m+n)\\
T_{m, n} &\leq E[\![2c(m_{1} + n')]\!] + E[\![2c(m_{2} + n')]\!] + c(m+n) \\
&= cm' + 2cn' + 2c\cdot E[\![m_{2}]\!] + 2cn' +c(m+n)\\
\text{Claim:} &E[\![m_{2}]\!] = 2(n'-1) \\
 &= cm' + 2cn' + 2c \cdot 2(n'-1) + 2cn' + c(m+n) \\
&= cm' + 8cn' + c(m+n) \\
&\leq 2c(m+n)
\end{align}
$$

With the claim, we have proved the assumption and hence we have that $T_{m, n} \leq 2c(m+n)$ and hence is in $O(|E|)$ and we are done. 

Now we are just left with the proof of the claim.

To prove the claim we analyze a different algorithm that constructs a similar "good enough spanning tree" but where finding the expected value of $m_{2}$ would be easy.

The algorithm is a modification of Kruskal's Algorithm.
1. Sort the edges according to weights
2. Start from least weighted edge and do the following
	1. If the edge is $F$-heavy where $F$ is forest formed till the current step. We move forward
	2. Otherwise, we toss a coin, if tails we move forward, if heads we attempt to add it to $F$

This algorithm mimics the previous one because the algorithm forms a non-optimal spanning tree $F$, which is similar to $F_{1}$. 
- An edge being $F$-heavy means it forms a cycle with other vertices that are lighter, which means checking if an edge is $F$-heavy after adding only the edges lighter that it is enough. We also don't attempt to add it to the tree as they are going to make a cycle.
- If an edge is not $F$-heavy we flip a coin before attempting to add it. This is the as filter out the edges while creating $E_{1}$, ones that get tail here, would be ones that were not a part of $E_{1}$ hence did not get added to the tree, the other ones are added to the tree because if they would have made a cycle, it would have been with all smaller vertices, and hence would make the edge an $F$-heavy edge.

Given the above, the expected number of coin toss is twice the number of edges, so we get $E[\![m_{2}]\!]=2(n'-1)$ and we are done.


---
# References
[[Karger, Klein and Tarjan's Algorithm]]