---
tags:
  - Note
---
202510060110

Tags : [[Homotopy Type Theory]]
# Images are stable under pullbacks
---
>[!theorem]
>Consider functions $f:A\to B,g:C\to D$ and the diagram
>![[Pasted image 20251006011131.png|200]]
>If the outer rectangle is a pullback, then so are the inner squares. Consequently images are stable under pullbacks.

Assuming the outer square is a pullback we have the following:
$$
\begin{align}
B \times_{D} \text{im}_{n}(g) &\equiv \sum_{b:B} \sum_{w:\text{im}_{n}(g)} h(b)=\text{pr}_{1}(w) \\
&\simeq \sum_{b:B}\sum_{d:D} \sum_{w:\|\text{fib}_{g}(d)\|_{n}} h(b)=d \\
&\simeq \sum_{b:B}\|\text{fib}_{g}(h(b))\|_{n} \\
&\simeq \sum_{b:B} \|\text{fib}_{f}(b)\|_{n} \\
&\equiv\text{im}_{n}(f)
\end{align}
$$

---
# References
- [[Lemma for fibers of maps of pullbacks]]