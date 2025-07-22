---
tags:
  - Example
---

202507141632

tags : [[Category Theory]]
#  Corollaries of RAPL
---
>[!example]
>For any function $f:A\to B$, the inverse image $f^{-1}:PB\to PA$, a function between powersets of $A$ and $B$, preserve both unions and intersections while the direct image $f_{*}:PA\to PB$ only preservs the union.
>
>This is because unions are limits and intersections are colimits in the poset category $PA$. We are supposed to think of the functions as the following functors:
>![[Pasted image 20250714163634.png|150]]

>[!example]
>For any vector space $U, V, W$.
>$$
>U \otimes (V \oplus W)\cong (U \otimes  V) \oplus (U\otimes W)
>$$
>
>The two variable adjunction can be defined for the category of modules over any commutative ring, so also for vector spaces over a field. It follows that $U \otimes-:\text{Vect}\to\text{Vect}$ is left adjoint to $\text{Hom}(U,-)$ and consequently preserves the coproduct $V\oplus W$. This proves that tensor product distributes over coproducts in general.

>[!example]
>In general when categories have the product-exponent adjunction [[RAPL]] and [[RAPL|LAPC]] imply many arithmetic operations.

>[!example]
>The free-group on the set $X\sqcup Y$ is the free product of the free groups on the set $X$ and $Y$.

---
# Related
