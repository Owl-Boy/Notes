---
tags:
  - Note
---
202506071406

Tags : [[Category Theory]]
# Any Category with Coproducts and Coequalizers is Cocomplete, with Products and Equalizers is Compelte
---
>[!theorem]
>The Colimit of any small diagram $F:J \to C$ can be expressed as a coequalizer of pair of maps between the following coproducts.
>$$
>\coprod_{f\in \text{mor }J}F(\text{dom} f) \overset{d}{\underset{c}\rightrightarrows} \coprod_{j \in \text{ob }J} Fj\twoheadrightarrow \text{colim}_{J}\ F
>$$

To do so, we shall dualize the construction in [[Set is Complete]].

![[Pasted image 20250607150314.png|400]]

The component of $d$ at $f$ is defined to be the coproduct inclusion of the domain, while $c$ is the coproduct inclusion of the codomain of $f$. By hypothesis $C$ exists, we need to show that it is the colimit of $F$.

But because of [[Representation of Limits and Colimits as Limits in category of sets]](contravariant point 2), and the contravariant Yoneda embedding we get the following equalizer diagram:
![[Pasted image 20250607152059.png|400]]

Applying [[Representation of Limits and Colimits as Limits in category of sets]](contravariant point 1), we get for each object in the equalizer diagram:
![[Pasted image 20250607152543.png|400]]
When $X$ is fixed, we have get that evaluation function from [[Functor Categories inherit Limits and Colimits object-wise]], that is $\text{ev}_{X}:\text{Set}^C\to\text{Set}$ defines an equlizer in $\text{Set}$ and since [[Small Limits in Set are Equalizers]], considering the functor $\text{C}(F-,X):J^\text{op}\to\text{Set}$, we get that the above diagram constructs the limit 
$$
\text{lim}_{J^\text{op}}\text{C}(F-, X) \cong\text{C}(C, X)
$$
For each $X$. These isomorphisms assemble into isomorphism in $\text{Set}^{\text{ob }C}$ and from [[Functor Categories inherit Limits and Colimits object-wise]], the forgetful functor $\text{Set}^C\to\text{Set}^{\text{ob }C}$ creates all limits, hence $\text{C}(C, -)$ is the limit of the $J^\text{op}$ indexed diagram of covariant functors $\text{C}(Fj, -)$. Now [[Representable Universal Property of Colimits]] tell us that the coequalizer $C$ is the colimit of $F: J\to C$.

---
>[!theorem]
>Any category with all products and equalizers is complete.

---
# References
- [[Limits and Colimits]]
- [[Complete and Cocomplete Categories]]
- [[Representable Universal Property of Limits]]
- [[Representable Universal Property of Colimits]]
- [[Set is Complete]]
- [[Representation of Limits and Colimits as Limits in category of sets]]
- [[Functor Categories inherit Limits and Colimits object-wise]]
- [[Small Limits in Set are Equalizers]]
- [[Any category with Pullback and a terminal object has all finite limits, with pushouts and an initial object has all finite colimits]]