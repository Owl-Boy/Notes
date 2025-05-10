---
tags:
  - Note
  - Incomplete
---
202505060105

Tags : [[Category Theory]]
# Yoneda Embedding
---
>[!Theorem]
>The functors
>![[Pasted image 20250506010935.png|500]]
>define full and faithful embeddings.

Both of these are just components of teh common bifunctor 
$$
C(-,-) : C \times C^\text{op} \to \text{Set}
$$
The above embeddings are fully faithful if they define local bijections
$$
\begin{align}
C(c, d) \xrightarrow{\cong}\text{Hom}(C(-,c),C(-,d))\\
C(c, d) \xrightarrow{\cong}\text{Hom}(C(d,-),C(c,-))
\end{align}
$$

But it is easy to see that different morphisms would give different natural transformations.

By Yoneda's lemma we have that the natural transform $\alpha: C(d,-) \Rightarrow C(c,-)$ corresponds to an element in $C(c, d)$ . 

---
# References
