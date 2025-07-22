---
tags:
  - Note
---
202506141506

Tags : [[Category Theory]]
# Limits and Colimits in multiple variables can be taken in any order
---
Consider a functor of two variables $F:I \times J \to C$. Which can be regarded as $F:I \to C^J$ or $F: J\to C^I$.

Consider the case when $F:I\to C^J$. A limit of this diagram would be a $J$, shaped diagram in $C$, and then one can find a limit of that diagram, we denote this as $\text{lim}_{J}\text{lim}_{I}\ F$.
Similarly $F:J\to C^I$, we can first find a limit of the diagram of shape $J$, which would be a diagram of shape $I$ evaluated in $C$. The limit of that can be denoted as $\text{lim}_{I}\text{lim}_{J}\ F$.

>[!theorem]
>If the limits $\text{lim}_{I}\text{lim}_{J}\ F$ and $\text{lim}_{J}\text{lim}_{I}\ F$ associated with a diagram $F:I\times J \to C$ exist, then they are isomorphic define $\text{lim}_{I\times J}\ F$.

As an example, if $I = \bullet \rightrightarrows \bullet$ is and $J=\bullet \rightarrow \bullet \leftarrow \bullet$, then we get $I\times J$ is
![[Pasted image 20250614160943.png|250]]

And the two limits would look like 
![[Pasted image 20250614161555.png]]

By [[Yoneda Lemma]] it is sufficient to prove that 
$$
C(X, \lim_{i\in I}\lim_{j\in J} F(i, j)) \cong C(X, \lim_{(i, j)\in I\times J} F(i, j)) \cong C(X, \lim_{j \in J}\lim_{i \in I} F(i, j)) 
$$
And by [[Representable Universal Property of Limits]] we get
$$
C(X, \lim_{i\in I}\lim_{j\in J} F(i, j)) \cong \lim_{i\in I}C(X, \lim_{j\in J} F(i, j)) \cong \lim_{i\in I}\lim_{j\in J}C(X, F(i, j))
$$
We have reduced the problem to proving when the codomain of the functor is $\text{Set}$, and consider the functor $H(i, j):= C(X, F(i, j))$, so we get 
$$
\lim_{i \in I} \lim_{j \in J} H(i, j) \cong  \lim_{(i, j) \in I\times J} H(i, j) \cong \lim_{j \in J} \lim_{i \in I} H(i, j)
$$
And it suffices to prove the left isomorphism.

By definition $\lim_{(i,j)\in I \times J} H(i, j)$ is the set of cones with summit $1$ over the diagram indexed by $I\times J$.

The set $\lim_{i \in I}\lim_{j \in J} H(i, j)$ is the set of cones with summit $1$ over $I$ indexed diagrams $\lim_{j\in J}H(-, j)$ which is made of legs
$$
\Big(1 \xrightarrow {\lambda_{i}} \lim_{j \in J} H(i, j) \Big)_{i\in I} 
$$
which commute with the map of limits $\text{lim}_{j\in J}H(i, j)\to\text{lim}_{j\in J}H(i', j)$ determined by a morphism $i\to i'$. The map of limits is defined in [[Choosing Limits of diagrams in Functorial]].

By definition of universal property of $J$-indexed limits, to define a limit cone leg $\lambda_{i}$, one needs to define it by the following.
$$
\Big(1 \xrightarrow {\lambda_{i,j}} H(i, j) \Big)_{j\in J} 
$$
which must commute with the map $H(i, j)\to H(i, j')$ induced by $j\to j'$. Thus the total data is precisely the cone:
$$
\Big(1 \xrightarrow {\lambda_{i,j}} H(i, j) \Big)_{(i, j)\in I\times J} 
$$
Thus we are done.

We get the theorem for colimits by duality.

---
# References
- [[Yoneda Lemma]]
- [[Representable Universal Property of Limits]]
- [[Choosing Limits of diagrams in Functorial]]
- [[Colimit of Limits gives Limit fo Colimit of a Bifunctor]]