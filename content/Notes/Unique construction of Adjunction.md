---
tags:
  - Note
---
202507071507

Tags : [[Category Theory]]
# Unique construction of Adjunction
---
>[!theorem]
>Consider a functor $F:A\to B$ such that for each $b:B$ there is an object $Gb:A$ such that the following isomorphism exists:
>$$
>B(Fa, b) \cong A(a, Gb)
>$$
>Then there is a unique way to extend the assignment $G:\text{ob }B \to\text{ob }A$ such that the family of isomorphisms in natural in $B$.

[[Natural Transformation|Naturality]] in $B$ demands 
$$
A(a, Gb)\cong B(Fa,b)\xrightarrow{f_{*}}B(Fa, b')\cong A(a, Gb')
$$
equal composition by a morphism $Gf:Gb\to Gb'$. This defines the natural transformation $A(-,Gb)\Rightarrow A(-,Gb')$, which must equal post composition by a unique morphism $Gf$ in $A$. this implies that the assignment $G:\text{mor }B\to\text{mor }A$ is functorial as defined in [[Categorization of Equivalent Categories]].

We thus get the [[Adjunctions|adjunction]] $F\dashv G$.

---
# References
- [[Natural Transformation]]
- [[Categorization of Equivalent Categories]]
- [[Adjunctions]]
- [[Mutual Left and Right Adjunctions]]