---
tags:
  - Note
---
202504102004

Tags : [[Finite Model Theory]]
# Monotonicity is Undecidable
---
>[!lemma]
>Testing if $F_{\varphi}$ is monotone is undecidable for $\text{FO}$ formula $\varphi$.

Let $\Phi$ be an arbitrary sentence, and let $\varphi(S, x) = S(x) \to \Phi$. If $\Phi$ is valid, then $\varphi(S,x)$ is always true, hence $F_{\varphi}$ is monotone. If $\Phi$ does not hold on some structure, then on that structure $\varphi(S, x) = \lnot S(x)$, which is not monotone. Thus validity reduces to monotonicity, and by [[Trakhtenbrot's Theorem]], this is undecidable.

---
# References
