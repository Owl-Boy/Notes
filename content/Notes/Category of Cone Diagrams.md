---
id: Category of Cone Diagrams
aliases:
  - Category of Cone Diagrams
tags:
  - Note
---
202512301735

Tags : [[Category Theory]]
# Category of Cone Diagrams
---
Consider a small category $J$, we can create a category $J^\triangleright$ by adding an element to $J$ which serves as the nadir over the entire category. This can be constructed as the following pushout.

![[Cocone category pushout.png]]

This should be the "closest" extension of the diagram to a cone under it, and this is formalizes as follows:

> [!THM]
> A category $C$ admits all colimits of diagrams indexed by a small category if and only if the restriction functor $C^{J^\triangleright}\to C^J$ admits a left-adjoint, defined by the left kan-extension

We have a fully faithful inclusion $J\hookrightarrow J^\triangleright$. Consider a diagram $F:J\to C$. For $j\in J\subseteq J^\triangleright$, the colimit defining the left kan extension always exists, which is just $F j$. For the cone point $t\in J^\triangleright$, the comma category $J\downarrow t$ is isomorphic to $J$, by construction. So if $\text{colim}(J\xrightarrow F C)$ exists, then we know that the values define the left kan extension, which can be defined as the colim functor.

---
# References

