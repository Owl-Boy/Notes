---
tags:
  - Note
---
202510081510

Tags : [[Homotopy Type Theory]]
# Reflective Subuniverses
---
>[!definition]
>A **Reflective Subuniverse** is a predicate $\mathcal U \to\text{Prop}$ such that for every $A:\cal U$, there is a type $\bigcirc A$ such that $P(\bigcirc A)$ and a map $\eta_{A}:A\to\bigcirc A$, with the property that for every $B:\cal U$ such that $P(B)$ the following function is an equivalence:
>$$
>\begin{cases}
> & \bigcirc A \to B  & \longrightarrow  & A\to B \\
> & f & \longmapsto & f\circ \eta_{A}
>\end{cases}
>$$

We write $\mathcal U_{P}:\equiv \{ A:\mathcal U\mid P(A) \}$ and also have $\text{rec}_{\circ}$ as the quasi inverse of the above map

The following facts about [[Reflective Subcategory|reflective subcategories]] are also true for **reflective subuniverses**:
- A type $\mathcal A$ lies in $\mathcal U_{P}$ iff $\eta_{A}$ is an equivalence.
- $\mathcal U_{P}$ is closed under retracts. If $\eta_{A}$ admits a retract then $A$ lies in $\mathcal U_{P}$,
- The operation $\bigcirc$ is functor in a suitable up-to-coherent homotopy, which can be made as precise as necessary. 
- The types in $\mathcal U_{P}$ are closed under all limits. In particular if $A: \mathcal U_{P}$ and $x,y:A$ then $x=y:\mathcal U_{P}$ as it is a pullback for $x, y:\mathbf{1}\to A$.
- Colimits in $\mathcal U_{P}$ can be constructed by applying $\bigcirc$ to colimits.

---
# References
