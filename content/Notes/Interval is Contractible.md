---
tags:
  - Note
---
202507131607

Tags : [[Homotopy Type Theory]]
# Interval is Contractible
---
>[!lemma]
>The type $I$ is [[Contractible Types|contractible]].

We pick $0_{I}$ to be the center of contraction and we now need to show that 
$$
\prod _{x:I}0_{I}=x
$$
but by recursion principle of the [[Interval (HoTT)|Interval]] we get
$$
\begin{align}
f(0_{I})&:\equiv \text{refl}_{0_{I}}: 0_{I}=0_{I} \\
f(1_{I})&:\equiv \text{seg}:0_{I}=1_{I}
\end{align}
$$
Now we need to define $\text{apd}_{f}(\text{seg})$ which should have the type $\text{seg}=_{\text{seg}}^{\lambda x.0_{I}=x}\text{refl}_{0_{I}}$. By definition the type is $\text{seg}_{*}(\text{seg})=\text{refl}_{0_{I}}$ , which is equivalent to $\text{seg}\cdot\text{seg}^{-1}=\text{refl}_{0_{I}}$ which we know is inhabited so we are done.


---
# References
- [[Interval (HoTT)|Interval]]
- [[Contractible Types]]