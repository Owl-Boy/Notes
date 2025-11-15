---
tags:
  - Note
---
202510052310

Tags : [[Homotopy Type Theory]]
# A function factorizes uniquely into an n-connected and an n-truncated function
---
>[!theorem]
>For each $f:A\to B$, the space $\text{fact}_{n}(f)$ defined by 
>$$
>\sum_{X:\cal U} \sum_{g:A\to X} \sum_{h:X\to B} (h\circ g \sim f) \times \text{conn}_{n}(g) \times \text{trunc}_{n}(h)
>$$
>is contractible. Its center of contraction is the element
>$$
>(\text{im}_{n}(f),\tilde{f},\pi_{1},\theta,\phi,\psi):\text{fact}_{n}(f)
>$$

By [[Every function factors through its n-image]], it suffices to show that the above type is a mere proposition. Suppose we have 2 $n$-factorizations
$$
(X_{1},g_{1},h_{2},H_{1},\phi_{1},\psi_{1})\quad\text{and}\quad(X_{2},g_{2},h_{2},H_{2},\phi_{2},\psi_{2})
$$
of $f$. Then we have the homotopy:
$$
H:(a\mapsto H_{1}(a)\cdot H_{2}(a)^{-1}):(h_{1}\circ g_{1}) \simeq (h_{2}\circ g_{2})
$$
By characterization of paths and transports in $\Sigma$-types, function types and path types, it suffices to show that:
1. An equivalence $e:X_{1} \simeq X_{2}$
2. A homotopy $\zeta: e\circ g_{1} \sim g_{2}$
3. A homotopy $\eta : h_{1}\circ e \sim h_{2}$
4. For any $a:A$ we have $\text{ap}_{h_{2}}(\zeta(a))^{-1}\cdot \eta(g_{1}(a))\cdot H_{1}(a)=H_{2}(a)$


For $1$ we have the fiberwise equivalence
$$
E(H):\prod_{b:B} \text{fib}_{h_{1}}(b)\simeq\text{fib}_{h_{2}}(b)
$$
By [[Lemma for unique factorization of functions]]. This induces the equivalence on total spaces 
$$
\left( \sum_{b:B}\text{fib}_{h_{1}}(b) \right) \simeq\left( \sum_{b:B}\text{fib}_{h_{1}}(b) \right)
$$
And we have $X_{1} \simeq \sum_{b:B}\text{fib}_{h_{1}}(b)$ and $X_{2} \simeq \sum_{b:B}\text{fib}_{f_{2}}(b)$, so we get what we want.

For 2, we choose $\zeta(a):\equiv\text{ap}_{\pi_{1}}(\bar{E}(H,a)):e(g_{1}(a))=g_{2}(a)$

For 3, we have $\pi_{2}(E(H,h_{1}(x))(x, \text{refl}_{h_{1}}(x))):h_{2}(e(x))=h_{1}(x)$. giving us the homotopy $\eta$.

For 4, by characterization of paths in fibers, the path $\bar{E}(H, a)$ gives us $\eta(g_{1}(a))=\text{ap}_{h_{2}}(\zeta(a))\cdot H(a)^{-1}$, the equality we want is trivial from the definition of $H$, we are done



---
# References
- [[Lemma for unique factorization of functions]]
- [[Every function factors through its n-image]]
- [[Fibers (HoTT)]]
- [[Higher Groupoid Structure of Pi Type]]
- [[Higher Groupoid Structure of Sigma Type]]
- [[Transports in a Family of Paths]]
- [[Higher Groupoid Structure of Identity Types]]