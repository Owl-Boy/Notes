---
tags:
  - Note
---
202504272104

Tags : [[Finite Model Theory]]
# $\text{FO}$ with Infinitary Connectives
---
This is an extension of [[First Order Logic|FO]] that lets us talk about arbitrary properties of cardinalities.

>[!definition] 
>The logic $\mathcal{L}_{\infty \omega}$ is defined as an extension of $\text{FO}$ with infinitary connectives $\bigvee$ and $\bigwedge$: If $\varphi_{i}$ is a formula for each $i$ in a potentially indexing set $I$, and free variables of all $\varphi_{i}$ belong to some $\vec{x}$, then the following are formulae
>$$
>\bigvee_{i\in I} \varphi_{i}\quad\quad \text{and} \quad\quad\bigwedge_{i\in I} \varphi_{i}
>$$
>
>The semantics are trivially extended.

This logic happens to be too powerful, thus is not of interest in finite model theory. That is shown by the following theorem:

>[!lemma]
>Let $\cal C$ be a class of finite structures closed under isomorphism. Then there is a $\mathcal{L}_{\infty \omega}$ sentence $\Phi_{C}$ such that $\mathfrak A \vDash \Phi_{C} \iff \mathfrak A \in \cal C$.

For every finite structure, one can write an [[First Order Logic|FO]] sentence that is modelled only by the structure and its isomorphic structures. This one can take the disjunction of all such formulae for structures in $\cal C$.

---
# References
