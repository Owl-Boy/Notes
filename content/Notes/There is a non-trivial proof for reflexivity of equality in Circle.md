---
tags:
  - Note
---
202507131707

Tags : [[Homotopy Type Theory]]
# There is a non-trivial proof for reflexivity of equality in Circle
---
>[!theorem]
>There exists an element $\prod_{(x:\mathbb S^1)} x=x$ which is  not equal to $x\mapsto\text{refl}_{x}$.

We define $f:\prod_{x:\mathbb S^1}x=x$ by induction. we let $x\equiv\text{base}$ and $f(x):\equiv\text{loop}$. Now we need to show $\text{transport}^{x \mapsto  x=x}(\text{loop},\text{loop})=\text{loop}$ but we have the following stronger statement
>[!lemma]
>$$
>\text{transport}^{x\mapsto x=x}(p,q)=p^{-1}\cdot q\cdot p
>$$


which holds by path induction on $p$. 

So we get that the transport evaluates to $\text{loop}^{-1}\cdot\text{loop}\cdot\text{loop}=\text{loop}$. which is clearly true.

To show $f\neq x\mapsto\text{refl}_{x}$ we show that $f(\text{base})\neq\text{refl}$ but we showed that $f(\text{base})=\text{loop}$ so we are done.

---
# References
- [[Circle (HoTT)|Circle]]
- [[Transport]]
- [[Universe with circle is not a groupoid]]