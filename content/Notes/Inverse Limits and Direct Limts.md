---
tags:
  - Note
  - Incomplete
---
202505161605

Tags : [[Category Theory]]
# Inverse Limit
---
>[!definition]
>The limit of the diagram indexed by the category $\omega^\text{op}$ is called the **inverse limit** of the sequence of morphisms.

A diagram indexed by the above category looks like:
$$
\dots\longrightarrow F_{3} \longrightarrow F_{2} \longrightarrow F_{1} \longrightarrow F_{0}
$$

A cone over this diagram is an extension of the diagram of shape $(\omega +1)^\text{op}$ which looks like:
![[Pasted image 20250516163018.png]]
The inverse limit is the terminal cone and is denoted as $\underset{\longleftarrow}\lim F_{n}$. Similar applies to any ordinal.

>[!example]
>The *p-adic integers* are defined to be the inverse limit of the following diagram of rings:
>$$
>\mathbb{Z}_{p} = \underset\longleftarrow\lim \mathbb{Z} /p^n \twoheadrightarrow \dots\twoheadrightarrow \mathbb{Z} /p^4 \twoheadrightarrow \mathbb{Z} /p^3 \twoheadrightarrow \mathbb{Z} /p^2 \twoheadrightarrow \mathbb{Z} /p
>$$
>Where the morphisms are the canonical quotient maps.

>[!definition]
>The colimit of a diagram indexed by the ordinal category $\omega$ is called the **Sequential Colimit** or the **Direct Limit**

The colimit of a diagram 
$$
F_{0} \longrightarrow F_{1} \longrightarrow F_{2} \longrightarrow F_{3} \longrightarrow \cdots
$$
is frequently denoted as $\underset{\longrightarrow}\lim F_{n}$, defines a diagram of shape $\omega+1$.

---
# References
