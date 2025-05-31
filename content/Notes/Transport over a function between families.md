---
tags:
  - Note
---
202505302305

Tags : [[Homotopy Type Theory]]
# Transport over a function between families
---
>[!lemma]
>Given:
>- A type $X$
>- A path $p:x_{1}=_{X}x_{2}$
>- Type families $A,B:X\to\cal U$
>- A function $f:A(x_{1}) \to B(x_{1})$ show that:
> 
>$$
>\text{transport}^{\lambda x.A(x)\to B(x)}(p, f) = x \mapsto \text{transport}^B(p, f(\text{transport}^A(p^{-1}, x)))
>$$

When we transport the function $f:A(x_{1}) \to B(x_{1})$ along $p$ we get a function $g:A(x_{2})\to B(x_{2})$ which can be defined by 
- starting with an element in $A(x_{2})$
- moving it to $A(x_{1})$ along $p^{-1}$
- moving it to $B(x_{1})$ using $f$
- moving it to $B(x_{2})$ along $p$.

---
# References
[[Transport]]
[[Higher Groupoid Structure of Pi Type]]
