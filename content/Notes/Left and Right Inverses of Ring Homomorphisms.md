---
tags:
  - Note
---
202507031507

Tags : [[Module Theory]], [[Homology Theory]]
# Left and Right Inverses of Ring Homomorphisms
---
>[!lemma]
>Let $\varphi: M\to N$ be an $R$-[[Modules]] homomorphism. Then
>- $\varphi$ has a left-invese iff the following sequence [[Split Exact Sequences|splits]]
>  $$
>  0 \longrightarrow M \xrightarrow{\;\varphi\;} N\longrightarrow \text{coker}\ \varphi\longrightarrow 0
>  $$
>- $\varphi$ has a right-invese iff the following sequence [[Split Exact Sequences|splits]]
>  $$
>  0 \longrightarrow \text{ker}\ \varphi \longrightarrow M \xrightarrow{\;\varphi\;} N\longrightarrow 0
>  $$

For the first part, if the sequence splits, the one can get $M$ back using the projection.

If $\varphi$ has a left-inverse, then we can write the following diagram:
![[Pasted image 20250703160135.png|200]]
We now need to show that $N$ is isomorphic to $M \oplus\text{coker }\varphi$. We first get a unique morphism from $N$ to $M\oplus\text{coker }\varphi$ because of the map specified in the sequence and the inverse map, due to the [[Universal Property of Products and Coproducts|universal property of products]].

Now we can define maps from  $M\to N$, which is the inverse, and $\text{coker }\varphi \to N$. For the second one, consider the inverse image of an element $a$ in the cokernel. This be the element that goes to $a$ in the cokernel and that goes to $0$ in the inverse image to $M$. The uniqueness of this comes from the universal property of [[Kernels and Cokernels]]. No using the [[Universal Property of Products and Coproducts|universal property of coproducts]], we get a unique map from $M \oplus\text{coker }\varphi$.

The other direction seems to be the dual.

---
# References
- [[Modules]]
- [[Split Exact Sequences]]
- [[Kernels and Cokernels]]
- [[Universal Property of Products and Coproducts]]
- [[Direct sum of Modules]]