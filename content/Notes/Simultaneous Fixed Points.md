---
tags:
  - Note
  - Incomplete
---
202504150604

Tags : [[Finite Model Theory]]
# Simultaneous Fixed Points
---
**Simultaneous Fixed Points** are a tool that allow us to iterate over several formulae at once.

>[!definition]
>Let $\sigma$ be a relational vocabulary, and $R_{1}, R_{2} \dots R_{n}$ be additional symbols with $R_{i}$ having arity $k_{i}$. Let $\vec{x}_{i}$ be a tuple of length $k_{i}$ and consider the following sequence of formulae:
>$$
>\begin{align}
>\varphi_{1}(R_{1}, R_{2} &\dots R_{n}, \vec{x}_{1})\\
>&\cdots\\
>\varphi_{n}(R_{1}, R_{2} &\dots R_{n}, \vec{x}_{n})
>\end{align}
>$$
>Then for each $\varphi_{i}$, one can define an operator 
>$$
>F_{i} : \mathcal  P(A^{k_{1}}) \times \mathcal P(A^{k_{2}})\cdots \mathcal P(A^{k_{n}}) \to \mathcal P(A^{k_{i}})
>$$
>defined as
>$$
>F_{i}(X_{1}\dots X_{n}) = \{ \vec{a} \in A^{k_{i}} \mid \mathfrak A \vDash \varphi (X_{1} / R_{1}, \dots , X_{n}, R_{n}, \vec{a}) \}.
>$$
>which can be combined together into 1 operator defined as follows:
>$$
>F : \mathcal  P(A^{k_{1}}) \times \cdots  \times\mathcal P(A^{k_{n}}) \to \mathcal  P(A^{k_{1}}) \times \cdots \times \mathcal P(A^{k_{n}})
>$$
>
>given by
>$$
>F(X_{1}, \dots X_{n}) = (F_{1}(X_{1}, \dots X_{n}), \dots, F_{n}(X_{1},\dots,X_{n}))
>$$
>A sequence of sets $(X_{1} \dots X_{n})$ is a fixed point if it is a fixed point of $F$ and is the least fixed point if it is the component-wise least fixed point.

A logic that accommodates for such an operator is $\text{LFP}^\text{simult}$.

>[!example]
>Consider the property that is the set of nodes $(a, b)$ such that there is a path of even length between them.
>We define formulas to the following properties:
>- Given $x, y, z$, there exists a simple path from $x$ to $y$ that does not go over $z$.
>  $$\varphi_{1}(T, R, S, x, y, z) :\equiv \begin{align} (E(x, y) \land \lnot x=z \land \lnot y = z)  \\ \lor \exists u (E(x, u), T(u, y, z), \lnot(x=z))\end{align}$$
>- Given $x, y$, there is a simple path of odd length from $x$ to $y$
>  $$\varphi_{2}(T,R,S, x, y, z) :\equiv \begin{align} E(x, y) \\ \lor \exists u (S(x, u) \land E(u, y) \land T(x, u y))\end{align}$$
>- Given $x, y$ there is a simple path of odd length from $x$ to $y$
>  $$\varphi_{3}(T,R,S, x, y, z) :\equiv \exists u (R(x, u) \land E(u, y) \land T(x, u , y))$$
>
>Thus $[\text{lfp}_{S,\Phi}](x, y)$ expresses the query.


$\text{LFP}^\text{simult}$ makes it significantly more easy to describe constructions of complicated sets that require looking at multiple constructions. This begs the question:
- How much more powerful is $\text{LFP}^\text{simult}$ than $\text{LFP}$.

[[LFPsimult = LFP]]

---
# References
