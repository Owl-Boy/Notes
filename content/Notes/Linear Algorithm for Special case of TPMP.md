---
tags:
  - Note
  - Incomplete
---
202502182002

Tags : [[Verification of MST]], [[Topics in Algorithms]]
# Linear Algorithm for Special case of TPMP
---
## Preprocessing
We first start with some useful pre-processing:
- For each $v\in V$ we have a set $L_{v}$ and we can go through the list of pairs of points and we define $L_{v}=\{ i \mid v_{i} =v \}$. This can be done in $O(n)$ where $n$ is the size of the list by going through the list once.
- We can now traverse the tree and compute the height $h$. This can be done in time $O(m)$.

---
## $M_{v}$
The goal would be to efficiently construct $M_{v}$ for each $v\in V$ where:
$$
M_{v} = \{ j < d(v) \mid w(P_{v}(j)) > w(P_{v}(k)),\;\forall j<k<d(v) \}
$$
where
- $P_{v}(k)$ is the weight of the $k^\text{th}$ edge on the path from the root to the vertex $v$, note: $P_{v}(1)$ is the vertex that is attached to the root.

Intuitively, this is a list of position of heaviest edges on paths to $v$ from some $u$ in the path from root to $v$.

Once we do that, the answer for the queries simply becomes $\{ d(u) \}\downarrow M_{v}$. So the goal becomes to find $M_{v}$ for every $v$

But it is not known how to find $M_{v}$ efficiently, so we will find 2 kinds of sets:
- $D_{v} = \{ d(x) \mid x \text{ is an ancestor of }v \land v\text{ is an ancestor of } y, (x, y)\in \text{list}\}$
- $S_{v} = D_{v}\downarrow M_{v}$.

These are enough because $d(u)\in D_{v}$ so by we have that 
$$ \{ d(u)\} \downarrow S = \{ d(u) \}\downarrow(D_{v}\downarrow M_{v})=\{ d(v) \}\downarrow M_{v}
$$
which is exactly what we want, and these are going to be efficient to compute.

---
### $D_{v}$
$D_{v}$ can be defined recursively as:
$$
D_{v} = \{ d(u_{i}) \mid v_{i}=v\} \cup \bigcup_{u \text{ is a child of }v} 
(D_{u} \setminus \{ d(v) \})
$$
All of this can be done during a single tree-traversal, if we start to build the tree from the leaves to the top.

So this can be done  in time $O(m+n)$.

---
### $S_{n}$

We first make the observation that $M_{v}$ can be derived from $M_{u}$ by removing $0$ or more of the biggest elements and then adding $d(v)$. So $M_{v}\setminus M_{u}$ is just $\{ d(v) \}$ and hence $\sup (M_{v} \cap M_{u}) < \inf(M_{v} \setminus M_u)$ And so $(D_{v}\setminus D_u) \downarrow M_{u} \subseteq \{ d(u) \}\downarrow M_{n}=\emptyset$. 

For $S_{n}$ we first do the following simplifications, let $v$ be a non-root vertex and let $u$ be its parent:
$$
\begin{align}
S_{v} &= D_{v} \downarrow M_{v} \\
 &=_{(3)} ((D_{v}\cap D_{u}) \downarrow M_{v}) \cup ((D_{v}\setminus D_{u}) \downarrow M_{v})\\
 &\subseteq_{(3,5)} (D_{u} \downarrow M_{v} )\cup ((D_{v}\setminus D_{u}) \downarrow (M_{v}\setminus M_{u}))\\
&\subseteq_{(4)} (D_{u} \downarrow (M_{u} \cap M_{v})) \cup (D_{u}\downarrow (M_{u}\setminus M_{v})) \cup((D_{v}\setminus D_{u}) \downarrow (M_{v}\setminus M_{u})) \\
&\subseteq_{(7,1)} ((D_{u}\downarrow M_{u}) \cap M_{v}) \cup (M_{v} \setminus M_{u}) \\
&= (S_{u}\cap M_{v}) \cup \{ d(u) \} \\
&=\{ j\in S_{u} \mid w(P_{v}(j)) > w(v) \} \cup \{ d(u) \} \\
&= \{ j\in S_{u} \mid j \leq \sup \{ j' \in S_{i} \mid w(P_{v}(j')) > w(v) \} \} \cup \{ d(u) \}
\end{align}
$$
The last equality is justified by the fact that $S_{u}$ is a decreasing set, as the values increases, the weights of the edges at the indices decreases.

We define 
$$
R_{v} = \{ j\in S_{u} \mid j \leq \sup \{ j' \in S_{u} \mid w(P_{v}(j')) > w(v) \} \}
$$
and
$$
R_{v}' = \{ j\in S_{u} \mid j \leq \sup \{ j' \in D_{v}\downarrow S_{u} \mid w(P_{v}(j')) > w(v) \} \}
$$

Some information we have:
- We have showed that $S_{v}=D_{v}\downarrow M_{v} \subseteq R \cup \{ d(u) \} \subseteq M_{v}$, so we have that $D_{v}\downarrow M_{v}=D_{v}\downarrow R \cup \{ d(u) \}$ 
- And we have that $R$ is the intial segment of $S_{u}$, do $D_{v}\downarrow R \subseteq D_{v}\downarrow S_{u}$
- $R' \subseteq R$

Now let $j\in D_{v}\downarrow R$, If $j\not \in  R'$ then 
- $j > \sup \{ j'\in D_{v}\downarrow S_{u} \mid w(P_{v}(j')) > w(v) \}$
- Then $j > \sup \{ j'\in D_{v}\downarrow R \mid w(P_{v}(j')) > w(v) \}$
- So $j > \sup(D_{v}\downarrow R)$
This is a contradiction. So $D_{v}\downarrow R \subseteq R'$ so $D_{v}\downarrow R'= D_{v}\downarrow R$. But since $d(v)> \sup R$ we have that $S_{v}=D_{v}\downarrow (R' \cup \{ d(v) \})$.

![[Pasted image 20250219181132.png]]

We thus use the following definition.

During the traversal, the ancestors of a node currently visited are kept in an array sorted by depth, so it is easy to access $P_{v}(j')$.

The value of $\sup \{ j'\in D_{v}\downarrow S_{u} \mid w(P_{v}(j')) > w(v) \}$ is found using binary search. If $S =\emptyset$ then we return $-\infty$. Otherwise we compute the median of $S$, then we do the binary search thing, If the element we get satisfies the property, then we return its weight, otherwise we return $-\infty$.

During the visit of the node $v$ the algorithm answer queries of indices stored in $L_{v}$.

Outside of the binary search, each operation done on the list is $O(1)$.

Since $|S_{v}| \leq |D_{v}|$ for all $v\in V$ the complexity given will be $O\left( m+n+\sum_{v\in V}\log(|D_{v}|+1) \right)$ which by Komlos is $O(m+n)$

---
### Median of h-set
![[Pasted image 20250219184332.png]]


---
# References
