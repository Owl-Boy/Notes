---
tags:
  - Note
---
202507221707

Tags : [[Homotopy Type Theory]]
# Maps from Suspension to a space are isomorphic to maps from space to loop space
---
>[!theorem]
>For pointed types $(A,a_{0})$ and $(B, b_{0})$ we have
>$$
>\text{Map}_{*}(\Sigma A, B)\simeq \text{Map}_{*}(A, \Omega B)
>$$

The proof is a sequence of equiavlences, not going to write the entire thing but the gist of it is as follows:
$$
\begin{align}
\text{Map}_{*}(\Sigma A, B) :\equiv \sum_{f:\Sigma A\to B}f(N)=b_{0}
\end{align}
$$
And by universal property of suspension, to give a function from $\Sigma A \to B$ we only need to give 2 point $b_{n}$ and $b_{s}$ and a map $A\to b_{n}=b_{s}$, and the type also asks a proof for $f(N)\equiv b_{n}=b_{0}$ so concatenating them we get
$$
\text{Map}_{*}(\Sigma A, B)\simeq \sum_{b_{s}:B}A\to(b_{0}=b_{s})
$$
The rest of the proof is the following chain of equivalences
$$
\begin{align}
\sum_{b_{s}:B}A\to(b_{0}=b_{s}) &\simeq \sum_{(b_{s}:B)}\sum_{(g:A\to(b_{0}=b_{s}))}\sum_{(q:b_{0}=b_{s})}g(a_{0})=q \\
&\simeq \sum_{\left( r:\sum_{(b_{s}:B)}(b_{0}=b_{s}) \right)}\sum_{(g:A\to b_{0}=\text{pr}_{1}(r))}g(a_{0})=\text{pr}_{1}(r) \\
&\simeq \sum_{g:A\to b_{s}=b_{0}} g(a_{0}=\text{refl}_{b_{0}}) \\
&\equiv\text{Map}_{*}(A, \Omega B)
\end{align}
$$
thus we have proved the theorem.

---
# References
- [[Suspensions (HoTT)|Suspensions]]
- [[Loop Space]]
- [[Universal Property (Riehl)]]