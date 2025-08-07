---
tags:
  - Note
---
202507251707

Tags : [[Homotopy Type Theory]]
# Universal Property of Set Truncations
---
>[!theorem] 
>Given $B:\|A\|_{0}\to\cal U$ together with $g:\prod_{a:A}B(|a|_{0})$ and assume that each $B(x)$ is a set. Then there exists a function $f:\prod_{x:\|A\|_{0}}B(x)$ such that $f(|a|_{0})\equiv g(a)$.

It suffices to construct for any $x,y,z,w,p,q,r,s$ as above, a $2$-path $v:r=^B_{u(x,y,p,q)}$. However, by definition of dependent 2-path, this is an ordinary 2 path in the fibre of $B(y)$. Since $B(y)$ is a set, a 2-path exists between any pari or parallel paths.

---
>[!theorem]
>For any set $B$ and any type $A$, composition with $|-|_{0}:A\to\|A\|_{0}$ determines and equivalence
>$$
>(\|A\|_{0}\to B) \simeq (A\to B)
>$$

The special case of the theorem before this where $B$ is the constant family gives the map from right to  left, which is the right inverse of "compose with $|-|_{0}$" function from left to right.  To show that this is also a left inverse. Consider a function $h:\|A\|_{0}\to B$ and consider the composition and then reapplication of the previous theorem to give $h':\|A\|_{0}\to B$. Then we get that $h'(|a|_{0})=h(|a|_{0})$.

But the type $B$ is a set. For any $x:\|A_{0}\|$ the type $h(x)=h'(x)$ is a mere proposition, and hence also a set. So $h'(|a|_{0})=h(|a|_{0})$ implies $h(x)=h'(x)$ for all $x:\|A\|_{0}$ and hence $h=h'$.

---
# References
- [[Truncation]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
- [[Universal Property (Riehl)]]