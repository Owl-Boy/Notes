---
tags:
  - Note
---
202505161505

Tags : [[Category Theory]]
# Equalizers and Coequalizers
---
>[!definition]
>An **Equalizer** is the limit of a diagram indexed by a parallel pair of morphisms, that is $\bullet \rightrightarrows \bullet$.

A diagram of this shape is simply a pair of parallel morphisms $f,g:A \to B$. A cone over this diagram is a pair of morphism $a:C \to A$ and $b:C \to B$ such that $f \circ a = g\circ a = b$.  

Hence together, the cone of the above diagram can be thought of as an object $C$ with a morphism $a$ such that $f\circ a = g \circ a$
The Limit diagram can be given as:

$$
E \xrightarrow{\;\;h\;\;} A \underset g{\overset{f}\rightrightarrows} B
$$
This is also called an equalizer diagram.

[[Examples of Equalizers|Here are some examples]].

>[!definition]
>A **Coequalizer** is a colimit of a diagram indexed by a parallel pair category $\bullet \rightrightarrows \bullet$

The **Coequalizer** of a pair of morphisms $f, g: A \rightrightarrows B$ is the universal map $h:B \to C$ with the property that $h \circ f = h \circ g$, the diagram of the cone looks as follows:
$$
A \overset {f} {\underset {g} {\rightrightarrows}} B \xrightarrow{h}C
$$

---
# References
- [[Limits and Colimits]]
- [[Examples of Equalizers]]
- [[Examples of Coequalizers]]