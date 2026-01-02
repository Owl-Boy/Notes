---
id: Adjunctions as Kan extensions
aliases:
  - Adjunctions as Kan extensions
tags:
  - Example
---

202601021607

tags : [[Category Theory]]

#  Adjunctions as Kan extensions
---
If $F:C\leftrightarrows D:G$ is an adjunction with unit $eta:1\Rightarrow GF$ and counit $\epsilon : FG \Rightarrow 1$, then $(G, eta)$ is a left kan extension of the identity functor at $C$ along $F$ and $(F,\epsilon)$ is the right Kan extension of identity at $D$ along $G$.

Conversely if $(G, \eta)$ is a left Kan extension of the identity along $F$ and if $F$ preserves this Kan extension then $F\dashv G$ with unit $\eta$.

---
# Related
- [[Kan Extensions]]
- [[Adjunctions]]

