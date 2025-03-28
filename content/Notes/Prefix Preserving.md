---
tags:
  - Note
  - Incomplete
---
202503232203

Tags : [[Weighted Automata and Transducers]]
# Prefix Preserving
---
A function from $A^* \to B^*$ is *Prefix Preserving* if it satisfies the following conditions:
- If $u \leq v$ and $v\in \text{dom}(f)$ then $u\in \text{dom}(f)$
- If $u\leq v$ then $f(u) \leq f(v)$

>[!theorem]
>Let $f$ be a sequential function, then $f$ is pure sequential iff
>- $f(\epsilon)=\epsilon$
>- $f$ is prefix preserving

***Proof:***
A pure sequential function clearly satisfies the above condition.
For the other direction we can [[Normalizing a Transducer|normalize]] the the transducer. We do have that for this automata such that $m_{0}=\epsilon$ and $\rho(q)$ is $\epsilon$. Other wise the prefix preserving properties don't hold. Hence the transducer is pure sequential. 

---
# References
