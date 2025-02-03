---
tags:
  - Note
---
202502030102

Tags : [[Finite Model Theory]], [[Order Theory]]
# Even Atoms in Boolean Algebras
---
A [[Boolean Algebra]] is defined using a signature $\subseteq$ (which is equivalent to the $\leq$ for order theory). Then intended interpretation here is finite boolean algebras, which are boolean algebras which an isomorphism to $2^X$ for some finite set $X$.

To talk about boolean algebras we use the following definitions
- $\bot(x) \equiv \forall z (x \subseteq z)$
- $\top(x) \equiv \forall z (z \subseteq x)$
- $x \cup y = z \equiv (x \subseteq z) \land (y \subseteq z) \land \forall u\big[(x \subseteq u) \land (y \subseteq u) \to (z \subseteq u)\big]$
- $x \cap y = z \equiv (z \subseteq x) \land (z \subseteq y) \land \forall u\big[(u \subseteq x) \land (u \subseteq y) \to (u \subseteq z)\big]$
- $\text{atom}(x)\equiv \lnot \bot(x) \land \forall z \big[z \subseteq x \to z = x \lor \bot (z)\big]$
- $x= \bar{y}\equiv \forall z \big[\text{atom}(z) \to (z \subseteq x \lor z\subseteq y) \land \lnot(z \subseteq x \land z \subseteq y)\big]$

The query we are looking for is : $Q_{\text{atom}}^\text{even}$ which state that the set of atoms of the structure is even in size. 

This Query is definable in $(\text{FO}+<)_{\text{inv}}$ but not in $\text{FO}$, this is proven [[Definablity of Even Atoms|here]].

This shows that $(\text{FO}+<)_{\text{inv}}$ is strictly more expressible than $\text{FO}$.

---
# References
