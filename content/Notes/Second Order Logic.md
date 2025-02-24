---
tags:
  - Note
  - Incomplete
---
202502231902

Tags : [[Logic]], [[Finite Model Theory]]
# Second Order Logic
---
>[!info] Second Order Logic
>*Second Order Logic* is an extension of [[First Order Logic]] which allows quantification of relations.
>
>This subsumes [[First Order Logic]] so model checking in general is undecidable.

The following is a grammar for *Second Order Logic*:
$$
\begin{matrix}
\varphi & := & \lnot \varphi & | & \varphi \land \varphi & | & \varphi \lor \varphi & | & \varphi \Rightarrow \varphi a \\
 & | & \forall x. \varphi & |  & \forall R_{n}.\varphi & |  & \exists x. \varphi & | & \exists R_{n}.\varphi \\
 & | & t=t & | & r(t\dots t)
\end{matrix}
$$
Where $x$ is a first order quantification, $R_{n}$ is a second order quantification which a relation with arity $n$. $r$ is a relation that either belongs to the signature, or is quantified. The following is the grammar for a term $t$.
$$
\begin{matrix}
t & := & x & | & f(t \dots t)
\end{matrix}
$$

>[!example]
>Given the signature $\sigma = \{ E_{2} \}$ which is meant to be the edge relation of the graph, one can write the following:
>$$
>\begin{align}
>\exists P_{2}, [&\text{Path\_Axioms}(P) \\
& \land(\forall R_{2}, \text{Path\_Axioms}(R) \to\forall x\ y, P(x, y) \to R(x, y)) \\
 & \land \forall x\ y, P(x, y)]
>\end{align}
>$$
>
>Here we define:
>$$
>\begin{align}
>\text{Path\_Axioms}(P)\equiv &(\forall x, P(x, x)) && \text{Reflexive} \\
>\land &(\forall x\ y, E(x, y) \to P(x, y)) && \text{Contains }E \\
>\land &(\forall x\ y\ z, P(x, y) \land P(y, z) \to P(x, z)) && \text{Transitive} 
>\end{align}
>$$
>
>The formula defined above, states that a given graph is connected. i.e between any 2 edges there is a path.

>[!note]
>The semantics of Second Order logic and its fragments are a straightforward extension of [[Semantics of First Order Logic]].

---
# References
