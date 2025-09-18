---
tags:
  - Note
---
202508302308

Tags : [[Category Theory]]
# Split Coequalizer
---
>[!definition]
>A **split coequalizer** diagram consists of the maps 
>![[Pasted image 20250830233345.png|200]]
>so that $hf=hg$, $hs=1_{z}$, $gt=1_{y}$ and $ft=sh$.

>[!lemma]
>The underlying fork of a **split coequalizer** is a [[Equalizers and Coequalizers|coequalizer]]. This also forms an *absolute colimit*: Any functor preserves this coequalizer.

That is because given any other object $w$ and a split epimorphism $k$ to it, you have the canonical map $ks:z\to w$, that map makes the whole diagram commute as 
- $ksh=kft=kgt=k$

This makes the diagram a coequalizer and since the underlying folk being a coequalizer is a property of the diagram, and the diagram remains the same under functors, the image of the diagram under a functor will also give a coequalizer.

>[!example]
>Given any algebra $(A,\alpha:TA\to A)$ for a monad $(T, \mu, \eta)$ on $C$, the diagram:
>![[Pasted image 20250830235858.png|200]]
>defines a split coequalizer.

---
# References
- [[Equalizers and Coequalizers]]