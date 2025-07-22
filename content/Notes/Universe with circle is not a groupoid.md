---
tags:
  - Note
  - Incomplete
---
202507131807

Tags : [[Homotopy Type Theory]]
# Universe with circle is not a groupoid
---
>[!theorem]
>If the type $\mathbb S^1$ belongs to a universe $\cal U$ then $\cal U$ is not a groupoid

The type $\mathbb S_{1}=\mathbb S_{1}$ is in $\cal U$ by [[Univalence]]. So we show that $\mathbb  S^{1}\simeq\mathbb S^1$ is not a [[Sets in Type Theory|set]]. To do so we show that $\text{id}_{\mathbb S^1}=_{\mathbb S_{1}\simeq\mathbb S_{1}}\text{id}_{\mathbb S^1}$ is not a [[Mere Propositions|mere proposition]]. Since being an equivalence is a mere proposition, this type is equivalent to $\text{id}_{\mathbb S^1}=_{\mathbb S_{1}\to\mathbb S_{1}}\text{id}_{\mathbb S^1}$ which by function extensionality is equal to $\prod_{x:\mathbb S^1}(x=x)$, which contains two unequal element from [[There is a non-trivial proof for reflexivity of equality in Circle]].

---
# References
 - [[Circle (HoTT)|Circle]]
 - [[Groupoids]]
 - [[Univalence]]
 - [[Sets in Type Theory]]
 - [[Mere Propositions]]
 - [[There is a non-trivial proof for reflexivity of equality in Circle]]