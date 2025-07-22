---
tags:
  - Note
---
202507022207

Tags : [[Category Theory]]
# Unit and Counit as Universal Arrows
---
The definition of an [[Adjunctions]] comprises of a pair of anti-parallel functors $F:C \leftrightarrows D:G$ with the natural bijection;
$$
D(Fc, d) \cong C(c, Gd)
$$
This states that the functor $C(c,G-)$ is represented by the element $Fc:D$. [[Yoneda Lemma]] tells us that the natural isomorphism $D(Fc,-)\cong C(c, G-)$ is determined by an element of $C(c, GFc)$. The transpose of $1_{Fc}$ denoted as $\eta_{c}$, This implies that $\eta_{c}$ assemble together into components of $\eta:1_{C}\Rightarrow GF$.

>[!definition]
>Given adjunction $F \dashv G$, there is a natural transformation $\eta:1_{C}\Rightarrow GF$, called the **Unit**, whose components $\eta_{c}:c\to GFc$ at c are defined to be the transpose of $1_{Fc}$ 
>
>Dually, when we fix a $d:D$, we are able to construct the natural transformation $\epsilon:FG \Rightarrow 1_{D}$ called the **Counit**.

This property of adjunctions is in fact equivalent to the definition, so we have 
>[!definition]
>An **Adjunction** consists of an anti-parallel pair of functors $F:C\leftrightarrows D:G$, together with natural transformations $\eta:1_{C}\Rightarrow GF$ and $\epsilon: FG\Rightarrow 1_{D}$. satisfying the following identities:
>![[Pasted image 20250702225814.png|400]]

---
# References
- [[Unit and Counit as Singleton and Evaluation]]
- [[Adjunctions]]
- [[Yoneda Lemma]]