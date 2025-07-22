---
tags:
  - Note
aliases:
  - Right Adjoints Preserve Limits
  - Left Adjoint Preserves Colimits
  - LAPC
---
202507141607
Tags : [[Category Theory]]
# RAPL
---
Limits define representations for contravariant functors: The universal property of the limits of $F:J\to C$ characterizies the functor $C(-, \text{lim }F)$. Similarly the value of a right adjoint $G:D\to C$ on an object $d$ is determined by a characterization of contravariant representable functor $C(-, Gd)$. These obseravations suggest that  right ajoints and limits might interact nicely, and that is the case:
>[!theorem]
>Right Adjoints preserve limits.

Consider a diagram $K:J\to D$ admitting a limit cone $\lambda:\text{lim }K\Rightarrow K$ in $D$.

If we apply the right adjoint $G:D\to C$ we get a cone in $C$ which is $G\text{ lim }K\Rightarrow GK$. The theorem asserts that this is a limit cone. To prove this, consider another cone $\mu:c\Rightarrow GK$

So we need to find a function between $c$ and $G\text{ lim }K$ but since this is an adjunction we know what
$$
D(Fc, \text{lim }K)\cong C(c, G\text{ lim }K)
$$
We first see that $Fc$ also forms a cone over $K$ if it forms a cone over $FGK$ using naturality. This gives a factorization in $D$ that we can move back to $D$ using the functor $G$. And so, we are done.
$$
C^J(\Delta c, GK)\cong D^J(F\Delta c, K)\cong D^J(\Delta Fc,K)\cong D(Fc, \text{lim}_{J}K)\cong C(c, G\text{ lim}_{j}K)
$$
---
# References
- [[Limits and Colimits]]
- [[Adjunctions]]
- [[Preservation, Reflection and Creation of Limits]]
- [[Natural Transformation]]