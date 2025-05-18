---
tags:
  - Note
  - Incomplete
---
202505111305

Tags : [[Category Theory]]
# Universal Elements are Universal Elements
---
>[!theorem] 
>A covariant set-valued functor is representable iff its category of elements has an initial object. Dually,  a contravariant functor is representable iff its category of elements has a terminal object.

It is easy to see that if a functor $F$ is representable, then its [[Element Category]] has a initial object.

We have $F \cong \text{Hom}(c,-)$ so the $\int F \cong c/C$. There is an initial $(c, \text{id}_{c})$ hence there is an initial object in $\int F$.

For the other direction, consider a functor $F$ such that $\int F$ has an initial object $(c, e)$. Then we will show that the natural transformation $\Psi(e):\text{Hom}(c, -) \Rightarrow F$ as defined by [[Yoneda Lemma]] is a natural isomorphism.

Since $(c, e)$ is initial, for any $e'\in  Fd$ there is a unique morphism $(c,e) \to (c',e')$ hence a unique morphism $f:c\to d$ such that $Ffe = e'$. This exactly says that $\Psi(x)_{d}:\text{Hom}(c, d) \to Fd$ is an isomorphism. Injection is by uniqueness as given described above, surjection is because $(c,e)$ is an initial object, so there always is a morphism from $(c, e)$ to any $(d, e')$.

---
# References
