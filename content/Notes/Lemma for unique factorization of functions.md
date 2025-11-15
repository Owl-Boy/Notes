---
tags:
  - Note
---
202510052310

Tags : [[Homotopy Type Theory]]
# Lemma for unique factorization of functions
---
>[!lemma]
>Consider the following commutative diagram of functions:
>![[Pasted image 20251005231526.png|150]]
>With $H:h_{1}\circ g_{1} \sim h_{2}\circ g_{2}$, where $g_{1},g_{2}$ are $n$-connected and $h_{1},h_{2}$ are $n$-truncated. Then there is an equivalence
>$$
>E(H, b) : \text{fib}_{h_{1}}(b)\simeq\text{fib}_{h_{2}}(b)
>$$
>for any $b:B$, such that for any $a:A$ we have an identification
>$$
>\bar{E}(H, a) : E(H, h_{1}(g_{1}(a)))(g_{1}(a), \text{refl}_{h_{1}(g_{1}(a))})=(g_{2}(a), H(a)^{-1})
>$$
>The above type is insane to read, but its obvious, the equivalence of fibers takes image of $a$ under $g_{1}$ to image of $a$ under $g_{2}$

To find an equivalence $E$, for every $b:B$
$$
\begin{align}
\text{fib}_{h_{1}}(b) &\simeq \sum_{w:\text{fib}_{h_{1}}(b)} \big\|\text{fib}_{g_{1}}(\text{pr}_{1}(w))\big\|_{n} \\
&\simeq \left\|\sum_{w:\text{fib}_{h_{1}}(b)}\text{fib}_{g_{1}}(\text{pr}_{1}(w))\right\|_{n} \\
&\simeq\|\text{fib}_{h_{1}\circ g_{1}}(b)\|_{n}
\end{align}
$$
And since there is an obvious equivalence $\text{fib}_{h_{1}\circ g_{1}}(b) \simeq\text{fib}_{h_{2}\circ g_{2}}(b)$, this we get
$$
\text{fib}_{h_{1}}(b) \simeq \text{fib}_{h_{2}}(b)
$$
Now to show the equivalence for any $a:A$.

$$
\begin{align}
(g_{1}(a), \text{refl}_{h_{1}(g_{1}(a))}) &\overset = \mapsto \big((g_{1}(a), \text{refl}_{h_{1}(g_{1}(a))}), \big|(a, \text{refl}_{g_{1}(a)})\big|_{n}\big) \\
&\mapsto\big|\big((g_{1}(a), \text{refl}_{h_{1}(g_{1}(a))}), (a,  \text{refl}_{g_{1}(a)})\big)\big|_{n} \\
&\mapsto\big|(a, \text{refl}_{h_{1}(g_{1}(a))})\big|_{n} \\
&\overset=\mapsto \big|(a, H(a)^{-1})\big|_{n} \\
&\mapsto \big|\big((g_{2}(a), H(a)^{-1}), (a, \text{refl}_{g_{2}(a)})\big)\big|_{n}\\
&\mapsto \big((g_{2}(a), H(a)^{-1}), \big|(a, \text{refl}_{g_{2}(a)})\big|_{n}\big) \\
&\mapsto(g_{2}(a), H(a)^{-1})
\end{align}
$$


---
# References
- [[Homotopy(HoTT)]]
- [[n-connected types]]
- [[n-truncated functions]]