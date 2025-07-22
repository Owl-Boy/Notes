---
tags:
  - Note
---
202507022307

Tags : [[Category Theory]]
# Equivalent Definitions of Adjuctions
---
The two main definitions of adjunctoins are given in [[Adjunctions]] and [[Unit and Counit as Universal Arrows]].

Using those and an equivalence between the two, the following 4 definitions of adjunctions are equivalent.
- Two antiparallel functors $F$ and $G$ with the natural bijection $D(Fc, d)\cong C(c, Gd)$.
- Two antiparallel functors $F$ and $G$ with natural isomorphisms $\eta:1_{C}\Rightarrow GF$ and $\epsilon:FG \Rightarrow 1_{D}$
- A natural transformatoin $\eta:1_{C}\Rightarrow GF$ so that 
  $$D(Fc, d)\xrightarrow{G}C(GFc,Gd)\xrightarrow{(\eta_{c})^*}C(c, Gd)
  $$ defines an isomorphism for all $c$ and $d$.
- Dually, a natural transformation $\epsilon:FG \Rightarrow 1_{D}$ so that
  $$
  C(c, Gd)\xrightarrow{F}D(Fc, FGd)\xrightarrow{(\epsilon_{d})_{*}}D(Fc,D)
  $$
  defines an isomorphism for all $c$ and $d$.

---
# References
- [[Adjunctions]]
- [[Unit and Counit as Universal Arrows]]