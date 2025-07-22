---
tags:
  - Note
---
202507131707

Tags : [[Homotopy Type Theory]]
# Loop is not refl
---
>[!theorem]
>$\text{loop}\neq\text{refl}_{\text{base}}$

If $\text{loop}=\text{refl}$ then we get that all types are [[Sets in Type Theory|sets]] in the following way: Given a type $A$ and a point $a:A$ with a loop $p:a=a$. there is a function $f:\mathbb S \to A$ that sends $\text{base}$ to $a$ and $\text{loop}$ to $p$ but that would mean:
$$
p=f(\text{loop}) = f(\text{refl}_{\text{base}})=\text{refl}_{a}.
$$
This contradicts [[Double Negation Does Not Cancel]] so we are done.


---
# References
- [[Circle (HoTT)|Circle]]
- [[Sets in Type Theory]]
- [[Double Negation Does Not Cancel]]