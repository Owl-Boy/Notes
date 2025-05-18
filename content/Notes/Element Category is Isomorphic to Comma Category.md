---
tags:
  - Note
---
202505111305

Tags : [[Category Theory]]
# Element Category is Isomorphic to Comma Category
---
In the contravariant case, objects $(c, e)\in \int F$ are in bijection with the natural transformation $\Psi(x):C(-,c) \Rightarrow F$. A morphism from $\Psi(x)$ to another element $\Psi(x')$ is a natural transformation $\text{Hom}(-, c) \Rightarrow \text{Hom}(-, c')$ and by the [[Yoneda Embedding]], there is a morphism $f:c \to c'$ so that the triangle commutes.

![[Pasted image 20250511132132.png|400]]

>[!lemma]
>For $F: C^\text{op} \to \text{Set}$, the category of elements is isomorphic to the comma category
>$$
>\int F \cong \mathcal Y \downarrow F
>$$
>defined relative to the [[Yoneda Embedding]] $\mathcal Y:C \to \text{Set}^{C^\text{op}}$. and the object $F:\mathbb{1} \to \text{Set}^{C^\text{op}}$

In the covariant case we get the following diagram
![[Pasted image 20250511134325.png|400]]


---
# References
