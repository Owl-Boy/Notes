---
tags:
  - Note
---
202507191607

Tags : [[Category Theory]]
# A functor admits a left adjoint iff all its comma categories have an initial object
---
>[!theorem]
>A functor $U:A\to S$ admits a left adjoint iff for each $s\in S$, the comma category $s\downarrow U$ has an initial object.

The comma category $s\downarrow U$ is isomorphic to the [[Element Category]] for the functor $S(s, U-):A\to\text{Set}$. If a left adjoint $F$ exists, then the component of the unit as $s$ defines an initial object $\eta_{s}:s\to UFs$ in this category.

Conversely if $s\downarrow U$ admits an initial object, which we suggestively denote by $\eta_{s}:s\to UFs$. This defines the value of a functor $\text{ob } S\to\text{ob }A$, which we can extend to a functor using [[Unique construction of Adjunction]] to the functor that we call $F$.

Since $\eta_{s}$ is the initial object in $s\downarrow U$, this implies the existence and uniqueness of such a map. This also gives the unit natural transformation. 

This allows to to define the natural transformation $\phi:A(F-,-)\Rightarrow S(-,U-)$ with components
$$
\phi_{s,a}:A(Fs, A)\Rightarrow S(s, Ua)
$$
as in [[Equivalent Definitions of Adjuctions]]: given a map $g:Fs\to a$ in $A$, define
$$
\phi_{s, a}(g):=s\xrightarrow{\eta_{s}}UFs\xrightarrow{Ug}Ua
$$
Injectivity and surjectivity of $\phi_{s, a}$ follow from uniqueness and existence for the morphism $\eta_{s}$ to any particular object $s\to Ua$ in $s\downarrow U$. This proves the  adjunction.

---
# References
- [[Element Category]]
- [[Adjunctions]]
- [[Comma Category]]
- [[Equivalent Definitions of Adjuctions]]
- [[Unique construction of Adjunction]]