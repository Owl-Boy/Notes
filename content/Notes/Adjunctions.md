---
tags:
  - Note
---
202506271206

Tags : [[Category Theory]]
# Adjunctions
---
>[!definition]
>An **adjunction** is a pair of [[Functors]] that have a special relation to one another:
>A pair of functors $F:C\leftrightarrows D : G$ form an **adjunction** if there is, for every $c:C$ and $d:D$ there is a [[Natural Transformation|natural isomorphism]]
>$$
>D(Fc, d) \cong C(c, Gd)
>$$
>which is natural in both variables. Here way say that $F$ is the **left-adjoint** of $G$ and $G$ is the **right-adjoint** of $F$.

Also deriving from what seems to be music notation, we match up the functions across the natural isomorphism as follows:
$$
Fc \xrightarrow{\quad f^\sharp\quad}d \quad\quad\leftrightsquigarrow\quad\quad c \xrightarrow{\quad f^\flat\quad}Gd
$$
When categories $C$ and $D$ are locally isomorphic, $D(Fc,d)$ and $C(c, Gd)$ are both hom-sets and hence the natural bijection can be written as the natural isomorphism between the following functors:
![[Pasted image 20250627124908.png|300]]

which also makes it easier to make sense of naturality in the 2 variables, naturality is $D$ can be depicted by the commutative diagram:
![[Pasted image 20250627130604.png|300]]

and commutativity in $C$ can be depicted by the diagram:
![[Pasted image 20250627130630.png|300]]

>[!note]
>An Equivalent definition is given in [[Unit and Counit as Universal Arrows]].


---
# References
- [[Functors]]
- [[Natural Transformation]]
- [[Examples of Adjunctions]]
- [[Unit and Counit as Universal Arrows]]
- [[Equivalence between definitions of Adjunction]]