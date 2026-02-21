---
id: Yoneda Embedding
aliases: []
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
The above embeddings are fully faithful if they define local bijections.

So we have, by the definition of the yoneda embedding:
$$
\text{Hom}(c, d)=y_d(c)
$$

But by Yoneda lemma we have:
$$
\text{Hom}(\text{Hom}(-, c), y_d)\cong y_d(c)
$$

But $\text{Hom}(-, c)$ is just $y_c$, so we get our result.

To see that the Yoneda Embedding agrees with the lemma:
We have that the map $\Psi: \mathcal C(c, d) \to \text{Hom}(y_c\to y_d)$, thus given an $f:c\to d$ we have that $\Psi(f)$ is a natural transformation $y_c\Rightarrow y_d$. On any object $a$, the natural transformation component $\Psi(f)_a$ sends a function $g:a\to c$ to a function $a\to d$ given by 
$$
\Psi(f)_a(g) = Fg(f) = f\triangleright g
$$

Thus we have $\Psi(f) = f \triangleright -$

---
# References
- [[Yoneda Lemma]]
- [[Natural Transformation]]
- [[Functors]]
- [[Equivalence of Categories]]
- [[Applications of Yoneda Lemma]]
