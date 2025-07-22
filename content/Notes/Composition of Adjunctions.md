---
tags:
  - Note
  - Incomplete
---
202507111607

Tags : [[Category Theory]]
# Composition of Adjunctions
---
>[!theorem]
>Given 2 adjunction $F\dashv G$ and $F'\dashv G'$ 
>![[Pasted image 20250711163337.png|400]]
>the composites form the adjunction $FF'\dashv G'G$.

We can simply show the natural isomorphisms:
$$
E(F'Fc,e)\cong D(Fc, G'e)\cong C(c, GG'e)
$$

Another way would be to define the units and counits as follows:
$$
\begin{align}
\bar{\eta} &:= 1_{C}\xRightarrow{\eta}GF\xRightarrow{G \eta' F} GG'F'F \\
 \bar{\epsilon} &:= F'FGG \xRightarrow{F'\epsilon G'}F'G'\xRightarrow{\epsilon'}1_{E}
\end{align}
$$


---
# References
