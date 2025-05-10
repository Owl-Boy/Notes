---
tags:
  - Note
  - Incomplete
---
202505101305

Tags : [[Category Theory]]
# Tensor Product as Universal Properties
---
Fix $\mathbb k$-vector spaces $V$ and $W$ and consider the functor
$$
\text{Bilin}(V, W; -): \text{Vect}_{\mathbb k} \to \text{Set}
$$
That sends a vector space $U$ to the set of bilinear maps into $U$ from $V,W$.
Equivalently, the bilinear may be defined by currying one may define it as the linear map $V \to \text{Hom}(W, U)$. where the codomains are vector spaces of linear maps.
The representation of the functor $\text{bilin(V, W;-)}$ defines a vector spaces denoted as $V \otimes_{\mathbb k}W$, called the tensor product of$V$ and $W$. That is, the tensor product is defined the by isomorphism:
$$
\text{Vect}_{\mathbb k}(V \otimes_{\mathbb k} W, U) \cong \text{Bilin}(V,W;U),
$$
This tells us that the natural isomorphism is determined by an element of of $\text{Bilin}(V,W; U)$. which is the map $\otimes:V \times W \to V \otimes_{\mathbb k} W$. That is, the tensor product is the universal vector space equipped with a bilinear map from $V \times W$. The natural transformation is given by the following:
![[Pasted image 20250510141917.png|500]]
Tracking $1_{V\otimes W}$ around the commutative square reveals the following:
![[Pasted image 20250510142213.png|300]]

Moreover, the universal property also gives a construction for the tensor product. Suppose $V \otimes W$ exists, consider its quotient space spanned by taking quotient of the bilinear map $- \otimes -$. That factors through the the quotient map $V \otimes W \to V \otimes W/\langle v\otimes w\rangle$ which is the $0$ map, but by naturality, they must agree. Hence $V \otimes W$ is the span of all $v \otimes w$ module the bilinearity relations satisfied by $- \otimes -$.

---
# References
