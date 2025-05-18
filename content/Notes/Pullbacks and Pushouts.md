---
tags:
  - Note
  - Incomplete
---
202505161505

Tags : [[Category Theory]]
# Pullbacks and Pushouts
---
>[!definition]
>A **Pullback** is a [[Limits and Colimits|limit]] of a diagram of shape $\bullet \rightarrow \bullet \leftarrow \bullet$.

A cone of this diagram with summit $D$ consists of a triple of morphisms such that both the triangles in the following diagrams commute:
![[Pasted image 20250516154744.png|150]]
Here the leg $a$ asserts that $gc = fb$

The **Pullback** is the universal cone over $f, g$, which is the commutative square with the following [[Universal Property (Riehl)|Universal Property]] : Given any commutative square, there is unique factorization through the summit of the pull back as 

![[Pasted image 20250516155313.png|200]]

$\lrcorner$ is the symbol used do denote that the square is a pullback.

The pullback $P$ is also called the **Fiber Product**, denoted as $B \times_{A}C$.

When $f:\mathbf{1} \to A$, then the pullback is called the **Fiber** of the map $g$ over the element $f$.

[[Examples of Pullbacks|Here are some examples]].

>[!definition]
>A **Pushout** is the colimit of a diagram of shape $\bullet \rightarrow \bullet \leftarrow \bullet$.

The diagram of a cone looks as follows
![[Pasted image 20250518174712.png|200]]

---
# References
