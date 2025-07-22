---
tags:
  - Note
---
202506161606

Tags : [[Homotopy Type Theory]]
# Similar description of inductive types lead to equal types
---
[[Natural Numbers in Type Theory]] were defined as 'the' natural numbers, but with induction types there is nothing stopping us from defining other types that look like natural types, for example the types $\mathbb{N}'$ defined using the constructors:
- $0':\mathbb{N}'$ 
- $\text{suc}' : \mathbb{N}'\to \mathbb{N}'$

This type feels the same, and in informal mathematics both the types would be used interchangeably, but one can prove that these types are equal, by giving functions $f:\mathbb{N} \to \mathbb{N}'$ which is an equivalence. The construction is straightforward and the proof for equivalence is similar to [[Uniqueness of functions created using induction principle]].

Similar ideas work even when the constructions are not that similar, like $[\mathbf{1}]$.
One can define $e_{0}':\equiv e_{\text{nil}}$ and $e'_{\text{suc}}:\equiv e_{\text{cons}}(\star)$, while defining $\text{suc}' :\equiv (\star::-)$ and the proof can be redone for this too.

Something similar can be done even if numbers are defined using binary. And with [[Univalence]], we get that all the types are equal.

In-fact similar constructions can be done for all [[Inductive Types]].

---
# References
- [[Inductive Types]]
- [[Uniqueness of functions created using induction principle]]
- [[Natural Numbers in Type Theory]]