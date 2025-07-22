---
tags:
  - Note
---
202506091606

Tags : [[Category Theory]]
# Cat and CAT are complete and Cocomplete
---
Product in either of the categories are described by the category product. The equalizer $E$ of a pair of parallel functors:
$$
E \rightarrowtail C \overset{F}{\underset{G}{\rightrightarrows}} D
$$
is a subcategory of objects $c$ of $C$ such that $Fc=Gc$ and all morphisms $f$ such that $Ff=Gf$.

Thus by applying [[Any Category with Coproducts and Coequalizers is Cocomplete, with Products and Equalizers is Complete]] we get that $\text{Cat}$  and $\text{CAT}$ are complete.

To show that they are co-complete, note that they have the category $\mathbb 1$ which is a terminal element, we now need to show that they have pushouts, but that is apparently hard.

---
# References
- [[Any Category with Coproducts and Coequalizers is Cocomplete, with Products and Equalizers is Complete]]
- [[Complete and Cocomplete Categories]]