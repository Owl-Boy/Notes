---
id: The Category of Garphs is Complete and Cocomplete
aliases:
  - The Category of Garphs is Complete and Cocomplete
tags:
  - Note
---
202512271920

Tags : [[Discrete Homotopy Theory]]
# The Category of Garphs is Complete and Cocomplete
---
The forgetful functor $(-)_V:\text{Graph} \to \text{Set}$ that takes a graph to its set of vertices is a forgetful functor.

The functor $\text{complete}:\text{Set} \to \text{Graph}$ takes a set to the graph made by attaching all vertices using edges. This functor happens to be the [[Adjunctions|left adjoint]] to the forgetful functor, while the functor $\text{discrete} : \text{Set} \to \text{Graph}$, which turns a set to the graph by only adding reflexive edges is the right adjoint to the forgetful functor.

Since $(-)_V$ has both adjoints, it preserves both limits and colimits due to [[RAPL]]. Thus, consider any diagram $D$ which is $\text{Graph}$ valued, that diagram can be taken to $\text{Set}$ using the forgetful functor. Now the limit can be taken back to the category $\text{Graph}$ using discrete functor and dually using the complete functor for any colimits.

Using this, we can construct any limit and colimit in the category of graphs.

---
# References
- [[Adjunctions]]
- [[Unit and Counit as Universal Arrows]]
- [[Complete and Cocomplete Categories]]
- [[RAPL]]
- [[Graph]]

