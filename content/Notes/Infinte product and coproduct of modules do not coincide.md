---
tags:
  - Note
  - Incomplete
---
202506220006

Tags : [[Module Theory]]
# Infinte product and coproduct of modules do not coincide
---
>[!theorem]
>Given a family of modules $\{ M_{a} \}_{a \in A}$ is a family of modules over teh set $A$. Let $\prod_{x:A}M_{a}$ be the categorical product and let $\coprod_{x:A}M_{a}$ be the categorical coproduct. Then show that these two do not coinicide.

The categorical product is selected by taking an element for each $a\in A$ from the set $M_{a}$. This is necessary because one can consider a map from $R$ to $M_{a}$.And that picks an element of $M_{a}$. Each map from $R\to M_{a}$ picks an element out of $M_{a}$, hence we pick $\prod_{A}M_{-}$ points. This set on inspection happens to satisfy the universal property.

For the categorical coproduct, given maps out of each $M_{a}$ we should get a map out of the coproduct. That would mean that we can pick our module as a sub-module of the product with only finitely many elements be non-zero. This satisfies the universal property of coproducts.

These two cannot condince. For example $|\mathbb{Z}^\mathbb{N}|>|\mathbb{Z}^{\oplus \mathbb{N}}|$.

---
# References
