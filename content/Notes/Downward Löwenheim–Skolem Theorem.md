---
id: Downward Löwenheim–Skolem Theorem
aliases:
  - Downward Lowenheim–Skolem Theorem
tags:
  - Note
---
202602102337

Tags : [[Model Theory]]
# Downward Löwenheim–Skolem Theorem
---
> [!THM] 
> Let $\sigma$ be a signature and let $|\sigma| = \lambda$. Let $\gamma > \lambda$. If there is a model of size $\lambda$ then there is a model of size $\kappa$ for every $\lambda \le \kappa \ge \gamma$.

Consider a model of size $\gamma$.

Consider any substructure $A$ of size $\kappa$.

We now use [[Axiom of Choice and its Variants|AOC]] to define the Skolem function $f_\varphi:M^n\to M$ for each formula $\varphi(y,x_1,\dots,x_n)$ such that it captures the a witness of $y$.

Thus for each formula $\varphi$, on the substructure $A$ we can define $F_\varphi(A) = A \cup f_\varphi(A)$ and we define $F(A)$ as $\bigcup F_\varphi(A)$.

Then we define $F^\omega$ as the closure of $F$.

Note that on each application, we add only $\kappa$ many more elements at most, for an infinite $\kappa$, and we do this at most countably many times. Thus we finally have a model of size $\kappa$ again.

This satisfies [[Tarski-Vaught test]] and hence is an [[Elementary Equivalence of Models|Elementary substructure]].

---
# References
- [[Upward Löwenheim–Skolem Theorem]]
- [[Tarski-Vaught test]]
