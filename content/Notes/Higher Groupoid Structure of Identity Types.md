---
tags:
  - Note
---
202505062105

Tags : [[Homotopy Type Theory]]
# Higher Groupoid Structure of Identity Types
---
We first start by noticing that equality respects equivalence
>[!theorem]
>If $f:A \to B$ is an equivalence, then for all $a,a':A$, so is
>$$
>\text{ap}_{f} : (a=a') \to (f(a)=f(a'))
>$$

To prove that, let $f^{-1}$ be the quasi inverse of $f$ with homotopies
$$
\begin{matrix}
\alpha:\prod_{(b:B)}f(f^{-1}(b))=b   & &  \text{and} &  & \beta: \prod_{a:A}f^{-1}(f(a))=a
\end{matrix}
$$
then we can let the quasi inverse of $\text{ap}_{f}$ to be $\text{ap}_{f^{-1}}$
This gives the following:
$$
\beta^{-1}(a) \cdot \text{ap}_{f^{-1}}(\text{ap}_{f}(p))\cdot \beta(a')= p
$$
We must also show that 
$$
\text{ap}_{f}(\beta^{-1}_{a} \cdot \text{ap}_{f^{-1}}(q) \cdot \beta_{a'}) = q
$$
The proof is as follows:
$$
\begin{align}
\text{ap}_{f}(\beta^{-1}_{a} \cdot \text{ap}_{f^{-1}}(q) \cdot \beta_{a'}) &= \alpha_{f(a)}^{-1} \cdot \alpha_{f(a)} \cdot 
\text{ap}_{f}(\beta^{-1}_{a} \cdot \text{ap}_{f^{-1}}(q) \cdot \beta_{a'}) \cdot \alpha_{f(a')}^{-1} \cdot \alpha_{f(a')} \\
&= \alpha_{f(a)}^{-1} \cdot \text{ap}_{f}( \text{ap}_{f^{-1}}(\text{ap}_{f}(\beta^{-1}_{a} \cdot \text{ap}_{f^{-1}}(q) \cdot \beta_{a'}))) \cdot \alpha_{f(a')} \\
&= \alpha_{f(a)}^{-1} \cdot\text{ap}_{f}(\beta_{a} \cdot \beta^{-1}_{a} \cdot \text{ap}_{f^{-1}}(q) \cdot \beta_{a'} \cdot \beta_{a'}^{-1}) \cdot \alpha_{f(a')} \\
&= \alpha_{f(a)}^{-1} \cdot \text{ap}_{f}(\text{ap}_{f^{-1}}(q)) \cdot \alpha_{f(a')} \\
&=q
\end{align}
$$

Hence if for some type $A$, if we have a full characterization of $a=a'$, then the type $p=_{a=a'}q$ is determined as well. 

For example for product types we have:
- Paths $p=q$, where $p,q: w =_{A\times B}w'$ are equivalence to pair of paths
  $$
  \text{ap}_{\text{pr}_{2}}p = \text{ap}_{\text{pr}_{2}}q \quad \text{and}\quad   \text{ap}_{\text{pr}_{2}}p = \text{ap}_{\text{pr}_{2}}
  $$
For depended function types we have 
- Paths $p=q$, where $p,q:f=_{\prod_{a:A}B(a)}g$ are equivalent to the homotopies
  $$
  \prod_{x:A}(\text{happly}(p)(x)=_{f(x)=g(x)} \text{ happly}(q)(x))
  $$

---
# References
- [[Types are Higher Groupoids]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
- [[Functions as Functors]]