---
tags:
  - Note
---
202510081610

Tags : [[Homotopy Type Theory]]
# Reflexive Subuniverse are closed under infinite products
---
>[!theorem] 
>If $B:A\to\mathcal U_{P}$ is a family of types in a [[Reflective Subuniverses]] $\mathcal U_{P}$, then $\prod_{x:A}B(x)$ is also in $\mathcal U_{P}$.

For every $x:A$ we can consider the function $\text{ev}_{x}:\left( \prod_{x:A}B(x) \right)\to B(x)$ defined by $\text{ev}_{x}(f):\equiv f(x)$. Since $B(x)$ lies in $P$, this extends to:
$$
\text{rec}_{\circ}(\text{ev}_{x}):\bigcirc \left( \prod_{x:A}B(x) \right)\to B(x)
$$
Then using the universal property of products we can define a function $h:\bigcirc\left( \prod_{x:A}B(x) \right)\to \prod_{x:A}B(x)$ by $h(z)(x):\equiv\text{rec}_{\circ}(\text{ev}_{x})(z)$. We now have that $h$ is a retraction of $\eta_{\prod_{x:A}B(x)}$, so we have that the product is in $\mathcal U_{P}$

---
# References
- [[Reflective Subuniverses]]
- [[Universal Property of Products and Coproducts]]
- [[Retracts (HoTT)]]