---
tags:
  - Note
---
202505292105

Tags : [[Homotopy Type Theory]]
# Fiber of a $\text{pr}_{1}$ of a $\Sigma$-Type
---
>[!lemma]
>For any type family $B:A \to \cal U$,  the fiber of $\text{pr}_{1}:\sum_{x:A}B(x)$ over the element $a:A$ is equivalent to $B(a)$.

$$
\begin{align}
\text{fib}_{\text{pr}_{1}}(a) &\equiv \sum_{u:\sum_{x:A}B(x)} \text{pr}_{1}(u)=a \\
&\simeq \sum_{x:A} \sum_{b:B(x)} x=a \\
&\simeq \sum_{x:A}\sum_{p:x=a}B(x) \\
&\simeq B(a)
\end{align}
$$

---
# References
- [[Fibers (HoTT)]]
- [[Dependent Pair Types|Sum Type]]
- [[Functions as Equivalences]]