---
tags:
  - Note
---
202502010002

Tags : [[Finite Model Theory]]
# Gaifman Theorem
---
This theorem makes locality of $\text{FO}$ explicit, by writing formulas such that it only attempts to talk about elements that are up to some distance $r$ from any witness for an existential operator.

>[!definition]
>We say $\varphi(\vec{x})$ is *r-local* around  $\vec{x}$ if all quantifications in $\varphi(\vec{x})$ are of the form $\exists y\in B_{r}(\vec{x})$ or $\forall y\in B_{r}(\vec{x})$. This is written as $\varphi^{(r)}(\vec{x})$.

>[!theorem]
>Let $\sigma$ be relational. Then every $\text{FO}$ formula $\varphi(\vec{x})$ over $\sigma$ is equivalent to a boolean combination of the following;
>- local formulae $\varphi^{(r)}(\vec{x})$ around $\vec{x}$
>- sentences of the form
>	- $$\exists x_{1} \dots x_{s} \left( \bigwedge_{i=1}^s \alpha^{(r)}(x_{i}) \land \bigwedge_{1 \leq i < j \leq s}d^{>2r}(x_{i}, x_{j})\right)$$
>Furthermore
>- the transformation from $\varphi$ to such a Boolean combination is effective;
>- if $\varphi$ itself is a sentence, then only sentences of the above form appear in the Boolean combination
>- if $\text{qr}(\varphi)=k$, and $n$ is the length of $\vec{x}$ then the bounds on $r$ and $s$ are $r \leq 7^k, s\leq k+n$.

Show [[Hanf-local Queries are Gaifman-local|FO is Gaifman-local]] is simply a straightforward corollary of this theorem.

This [[Gaifman-Locality]] can be strengthened in case of [[First Order Logic|FO]] to graphs with bounded degrees.

---
# References
