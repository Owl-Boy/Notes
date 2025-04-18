---
tags:
  - Note
---
202504111804

Tags : [[Finite Model Theory]]
# Arithmetic Operators are Definable in $\text{LFP}$
---
Given linear ordering, addition can be defined recursively using the successor relation that can be defined in [[First Order Logic|FO]].

>[!example]
>For $\mathbf{+}$ we use the recursive definition:
>$$
>\begin{align}
>x + 0 &= x \\
>x + (y+1) &= (x+y)+1
>\end{align}
>$$
>which can be given with the following relation.

Let $R$ be a ternary relation, we now define $\beta_{+}(R,x,y,z)$ can be defined as;
$$
\beta_{+}(R,x,y,z) = (y = \min \land\ z = x) \lor \exists u,\exists v,(R(x,u,v) \land \text{succ}(u, y) \land \text{succ}(v, z))
$$
now we can define the following as fixed point of the above operation.
$$
\varphi_{+}(u,v,w) = [\text{lfp}_{R,x,y,z}\beta_{+}(R,x,y,z)(u,v,w)]
$$
>[!example]
>For $\mathbf{\times}$ we use the recursive definition:
>$$
>\begin{align}
>x \times 0 &= x \\
>x \times(y+1) &= x \times y + x
>\end{align}
>$$

Let $R$ be a ternary relation, we now define $\beta_{\times}(R,x,y,z)$ can be defined as;
$$
\beta_{\times}(R,x,y,z) = (y = \min \land\ z = \min) \lor (R(x,u,v) \land \text{succ}(u, y) \land \beta_{+}(x,v,z))
$$
now we can define the following as fixed point of the above operation.
$$
\varphi_{\times}(u,v,w) = [\text{lfp}_{R,x,y,z}\beta_{\times}(R,x,y,z)(u,v,w)]
$$

---
# References
