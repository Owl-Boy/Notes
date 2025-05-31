---
tags:
  - Note
  - Incomplete
---
202505221205

Tags : [[Category Theory]]
# Set is Complete
---
Consider a diagram $F:J \to\text{Set}$. A limit is a representation of the functor:
$$
\text{Set}(X, \lim F) \cong \text{Cone}(X, F)
$$
which sends $X$ to cones over $F$ with summit $X$.

Since we also know that $\mathbf{1}$ is the initial element of the category we have 
$$
\lim F \cong \text{Set}(\mathbf{1}, \lim) \cong \text{Cone}(\mathbf{1}, F)
$$
Hence for any diagram we can simply define
>[!definition]
>Given a small diagram $F:J \to \text{Set}$ let
>$$
>\lim F := \text{Cone}(1, F)
>$$
>be the set of cones over $F$ with summit $\mathbf{1}$. We define the legs of the cone to be functions from $\text{lim } F \to Fj$
>$$
>\mu: \mathbf{1} \Rightarrow F \quad\mapsto \quad \mu_{j}:\mathbf{1} \to Fj
>$$

>[!note]
>$J$ being small is necessary because we want $\text{Set}^J$ to be locally small. Otherwise $\text{Cone}(X, F)$ would not be a set.

Now all we need to do is to prove that the above is actually the limit of $F$.

Consider a morphism $f:j \to k$ in $J$, then we need to show that the following diagram commutes:
![[Pasted image 20250522135834.png|250]]

For any element $\mathbf{1} \Rightarrow F$ we have the following 
$$
Ff(\lambda_{j}(\mu))=Ff(\mu_{j}) = \mu_{k} = \lambda_{k} \mu
$$
This proves that what we have defined is a cone over $F$.

To prove that this is the universal cone, consider another cone $\zeta: X \Rightarrow F$ with summit some $X$. We must show that $\zeta$ factors uniquely through $\lambda$ along $r:X \to \text{lim }F$.

For each element $x:X$ we can think of it as the function $x:\mathbf{1} \to X$, then there is a cone $\zeta x :\mathbf{1} \Rightarrow F$ that we get by restricting $\zeta$ to the element $x$.

We then get that $r(x) \in \text{lim }F$ to be $\zeta x$, by the definition of legs we get
$$
\lambda_{j}(r(x)) = \lambda_{j}(\zeta x) = (\zeta x)_{j} = \zeta_{j}x 
$$
Hence the cone factorizes through $\lambda$.

---
# References
