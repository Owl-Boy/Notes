---
tags:
  - Note
  - Incomplete
---
202505031505

Tags : [[Homotopy Type Theory]]
# Transport
---
We now extend the idea of [[Functions as Functors]], to dependent functions. This extension unfortunately is not trivial because given 2 elements $x, y:A$ such that $x=_{A}y$ the outputs $f(x)$ and $f(y)$ may belong to different types. To our rescue [[Path Induction#^4e1620|Indescernibility of Identicals]], which is the recursion principle for identity types.

>[!lemma] Transport
>Suppose that $P$ is a type family over $A$ and $p:x=_{A}y$, then there is a function $p_{*}:P(x) \to P(y)$

To construct the function, we only need to define it for the case when $p=\text{refl}_{x}$. We can simply have the function to be identity.

The transportation lemma corresponds to the "path lifting" operations in a [[Fibration]]... According to the book I am not sure how.

>[!lemma] Lemma: Path Lifting
>Let $P:A \to \cal U$ be a type family over $A$ and we have $u:P(x)$ for some $x:A$, then for any $p:x =_{A}y$ we have
>$$
>\text{lift}(u, p) : (x, u) = (y, p_{*}(u))
>$$
>in $\sum_{x:A}P(x)$, such that $\text{ap}_{\text{pr}_{1}}(\text{lift}(u, p)) = p$.

And we can now finally define the dependent version of [[Functions as Functors]].

>[!lemma]
>Suppose $f: \prod_{a:A}P(a)$, then we have the map:
>$$
>\text{apd}_{f}: \prod_{p:x=y}(p_{*}(f(x))=f(y))
>$$

---
# References
