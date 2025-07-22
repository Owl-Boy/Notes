---
tags:
  - Example
---

202507210139

tags : [[Category Theory]], [[Topology]]

#  Stone-Čech Compactification from Special Adjunct Functor Theorem
---
The [[Special Adjunct Functor Theorem]] is an abstraction of the construction of [[Stone Cech Compactification]] $\beta:\text{Top}\to\text{cHaus}$ which defines the left adjoint to the inclusion $\text{cHaus}\hookrightarrow\text{Top}$. The unit interval $I=[0,1]\in R$ is a coseparating object in $\text{cHaus}$. To see this, note that if $f\ne g:X\rightrightarrows Y$ then there must be a point $x\in X$ such that $f(x) \neq g(x)$. We can use [[Urysohn Lemma]] to find a map $h:Y\to I$ such that $f(x)\mapsto 1$ and $g(x)\mapsto 0$ .

Given a topological space $X$, [[Special Adjunct Functor Theorem]] construct an initial object in $X\downarrow\text{cHaus}$ in the following way.

A coseparating family in $X\downarrow\text{cHaus}$ is given by the set of maps $X\to I$. The product of these maps, considered as an object in $X\downarrow\text{cHaus}$, is the canonical map
$$
X \xrightarrow{\hat{\eta}} \prod_{\text{Hom}(X, I)}I
$$
A sub-object is a compact hausdorff space $K \subseteq \prod_{\text{Hom}(X, I)}I$ containing the image of $\hat{\eta}$. By since this object is compact hausdorff, its subspace is compact hausdorff iff it is closed. Hence the intersection of all sub-objects of $\hat{\eta}:X \to \prod_{\text{Hom}(X, I)}I$ is simply the codomain restriction $\eta:X\to \beta(X)$ where $\beta(X)$ is the closure of the image of $\hat{\eta}$.

This constructs the [[Stone Cech Compactification]]


---
# Related
- [[Special Adjunct Functor Theorem]]
- [[Stone Cech Compactification]]
- [[Slice Category]]
- [[Urysohn Lemma]]