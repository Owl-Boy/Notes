---
id: Yoneda Lemma as Kan extensions
aliases:
  - Yoneda Lemma as Kan extensions
tags:
  - Example
---

202601021612

tags : [[Category Theory]]

#  Yoneda Lemma as Kan extensions
---

From the definition of universal property, the right Kan extension of a functor $F$ along the identity is isomorphic to $F$. We also get that this Kan extension is pointwise., thus we can apply the limit formula to conclude that 
$$
Fc\cong \lim(c\downarrow C \xrightarrow \Pi C\xrightarrow F E)
$$
in any category E. When $E$ has products and equalizers, this limit can be expressed by giving the following equalizer diagram 
$$
Fc\rightarrow \prod_{c\to x}Fx\rightrightarrows \prod_{c\to x\to y} Fy
$$

Which is a generalization of the Yoneda Lemma. If the codomain in the category of sets, then its the standard Yoneda Lemma.

The dual of this statement gives us the coYoneda lemma : 
$$
Fc \cong \text{colim}(C\downarrow c\xrightarrow \Pi C \xrightarrow F E)
$$

---
# Related
- [[Kan Extensions]]
- [[Yoneda Lemma]]
- [[Pointwise Kan Extensions]]
