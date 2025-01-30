---
tags:
  - Note
  - Incomplete
---
202501271501

Tags : [[Finite Model Theory]]
# FO Queries are Hanf Local
---
>[!theorem]
>Every [[First Order Logic|FO]] Query $Q$ is [[Hanf-Locality|Hanf Local]]. Moreover if $Q$ is defined by an $FO[k]$ formula, then.
>$$
>\text{hlr}(Q) \leq \frac{3^k-1}{2}
>$$

The proof is by induction on the quantifier rank. If $k=0$ then $(\mathfrak A, \vec{a}) \leftrightarrows (\mathfrak B, \vec{b})$ means that $(\vec{a},\vec{b})$ defines a partial isomorphism between $\frak A$ and $\frak B$, and this $\vec{a}$ and $\vec{b}$ satisfy the same atomic formulas. Hence $\text{hlr}(Q)=0$ for $Q$ that are defined by $\text{FO}[0]$ formulas.

Suppose $Q$ is defined by a quantifier rank $k+1$. Such a formula is a boolean combination of formulae of the form $\exists z \varphi(\vec{x}, z)$ where $\text{qr}(\varphi)\leq k$. 

For the induction step, the proof is by contradiction, assume, for a query $Q$ or rank $k+1$, we have $\text{hlr}(Q)>3d+1$.  then we have the following.
$$
\begin{align}
&\mathfrak A &&\models \exists z\ \varphi(\vec{a}, z) \\
\implies&\mathfrak A &&\models \varphi(\vec{a}, c) & \text{for some }c \in A \\
\implies&\mathfrak B &&\models \varphi(\vec{b}, f(c)) \\
\implies&\mathfrak B &&\models \exists z\ \varphi(\vec{b}, z)
\end{align}
$$

And the same proof works in the other direction. From like 1 to line 2 the proof uses [[Local Equivalence Lemma]].

---
# References
