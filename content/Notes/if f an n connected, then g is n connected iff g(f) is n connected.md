---
tags:
  - Note
---
202509231509

Tags : [[n-connected types]]

# 2 out of 3 rule for n-connected functions
---
>[!lemma]
>Suppose that $f:A\to B$ is $n$-connected. Then $g:B\to C$ is $n$-connected if and only if $g\circ f$ is $n$-connected.

For any $c:C$ we have
$$
\begin{align}
\big\|fib_{g\circ f}(c)\big\|_{n} &\simeq \Big\|\sum_{w:\text{fib}_{g}(c)}\text{fib}_{f}(\text{pr}_{1}(w))\Big\|_{n} \\
&\simeq \Big\|\sum_{w:\text{fib}_{g}(c)}\|\text{fib}_{f}(\text{pr}_{1}(w))\|_{n}\Big\|_{n} \\ \\
&\simeq\big\|\text{fib}_{g}(c)\|_{n}
\end{align}
$$
The second equivalence is by [[Sum Types respect n-truncation]], and the third equivalence holds because $f$ is an $n$-truncation.

---
# References
- [[n-connected types]]
- [[Sum Types respect n-truncation]]