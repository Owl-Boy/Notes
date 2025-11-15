---
tags:
  - Note
---
202510041710

Tags : [[Parameterized Algorithms]]
# A parameterized problem is in FPT iff it admits a kernel
---
>[!theorem]
>A parameterized problem $Q$ is in [[Fixed Parameter Tractibility|FPT]] iff it admits a [[Kernelization|Kernel]].

If a kernelization algorithm exists, then the problem $Q$ is trivially in FPT, as doing the kernelization algorithm and then solving it would take time $P(n)+f(k)$ for some polynomial $P$ and some computable function $k$.

If a parameterized problem $(I, k)$ is in FPT, then it can be solved in time $f(k)|I|^c$ for some constant $c$ and computable function $f$. To get a kernelization algorithm for this, run the algorithm $\cal A$ on it for $|I|^{c+1}$ steps. If the algorithm terminates, use that to return if its a yes-instance or a no-instance. If the algorithm does not terminate, return $(I,k)$ as the output instance as $f(k)|I|^c > |I|^{c+1}$ this $f(k)>|I|$, thus we obtain a kernel of size at most $f(k)+k$

---
# References
- [[Parameterized Languages]]
- [[Kernelization]]