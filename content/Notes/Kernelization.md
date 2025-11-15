---
tags:
  - Note
---
202510041610

Tags : [[Parameterized Algorithms]]
# Kernelization
---
>[!definition]
>A **Kernalization Algorithm** (or a **kernel**) is an algorithm $\cal A$ that takes an input instance $(I, k)$ and in polynomial time, returns an equivalent instance $(I',k')$ of $Q$. And we have that $\text{size}_{\mathcal A}(k)<g(k)$ for some computable function $g$.

Kernelization Algorithm capture the idea of having a preprocessing step before running the "main" algorithm to solve the problem. For parameterized algorithms, a kernelization algorithm would involve taking a problem, and reducing it to another problem in time polynomial of $n$, to get a problem that can be solved under a computable function of $k$.

---
# References
- [[Parameterized Languages]]