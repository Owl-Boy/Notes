---
tags:
  - Note
  - Incomplete
---
202502020702

Tags : [[Finite Model Theory]]
# Invariant Queries
---
>[!definition]
>Let $\sigma$ and $\sigma'$ be 2 disjoint vocabularies, and let $\mathcal{C}$ be the class of all $\sigma'$ structures. A formula $\varphi(\vec{x})$ is called $\mathcal C$*-invariant* in the language of $\sigma \cup \sigma'$ on $\mathfrak A:\text{STRUCT}[\sigma]$ if for any 2 structures $C_{1}$ and $C_{2}$ of $\sigma'$ on $A$ in $\mathcal C$ we have:
>$$
>\mathfrak A, C_{1} \vDash \varphi(\vec{x}) \iff \mathfrak A, C_{2} \vDash \varphi(\vec{x})
>$$
>A formula is called $\mathcal C$-invariant, if it is $\mathcal C$-invariant of $\mathfrak A$ for any structure $\mathfrak A$

With a $\mathcal C$ invariant $\varphi(\vec{x})$, we have an associated query $Q_{\varphi}$ and it is given by 
$$
\vec{a}\in Q_{\varphi} \quad \text{iff}\quad (\mathfrak {A, A'}) \vDash \varphi(\vec{a})
$$
Where $\frak A'$ is some $\sigma'$ structure where the universe is $A$, by the invariance, it does not matter which one. 

One invariant logic of particular interest to us will be [[Order Invariant FO]] which is denoted by $(\text{FO} + <)_{\text{inv}}$.

---
# References
