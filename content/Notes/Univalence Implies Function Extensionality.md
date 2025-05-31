---
tags:
  - Note
aliases:
  - Weak Function Extensionality Implies Function Extensionality
---
202505300205

Tags : [[Homotopy Type Theory]]
# Univalence Implies Function Extensionality
---
>[!lemma]
>[[Weak Function Extensionality]] implies **Function Extensionality**.

We want to show that:
$$
\prod_{A:\cal U} \prod_{(P:A\to \cal U)} \prod_{(f, g):\prod_{x:A}P(x)} \text{is-equiv}(\text{happly}(f, g))
$$
Since a fiberwise map induces equivalence on total space if it is fiberwise an equivalence, by [[A Fiberwise Transformation is an Equivalence if its Total is an Equivalence]], we get:
$$
\left( \sum_{g:\prod_{x:A}P(x)}(f=g) \right) \to \sum_{g:\prod_{x:A}P(x)} f \sim g
$$
which is induced by $\gamma\left( g:\prod_{(x:A)}P(x) \right)$. We get $\text{happly}(f, g)$ is an equivalence, since the type on the left is contractible by [[Some Contractible Types]], it suffices to show that the type on right is contractibe, that is
$$
\sum_{g:\prod_{x:A}P(x)} \prod_{x:A}f(x)=g(x)
$$
But since [[Sigma Types respect Universal Properties]], the above is equivalence to
$$
\prod_{x:A} \sum_{u:P(x)} f(x) = u
$$
The equivalence requires function extensionality, but we can prove the former is the retract of the latter without function extensionality. 

The latter is a product of contractible types, so is a contractible type by weak function extensionality, thus we make the right hand side of the main equation a contractible, so we are done.

---
# References
- [[Univalence]]
- [[Weak Function Extensionality]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
- [[Contractible Types]]
- [[Some Contractible Types]]
- [[Sigma Types respect Universal Properties]]
- [[A Fiberwise Transformation is an Equivalence if its Total is an Equivalence]]