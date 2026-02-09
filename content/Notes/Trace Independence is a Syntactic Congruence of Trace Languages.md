---
id: Trace Independence is a Syntactic Congruence of Trace Languages
aliases:
  - Trace Independence is a Syntactic Congruence of Trace Languages
tags:
  - Note
---
202602051243

Tags : [[Concurrency Theory]]
# Trace Independence is a Syntactic Congruence of Trace Languages
---
Consider a trace alphabet $\bar\Sigma = (\Sigma, \mathcal I)$, which induces the trace equivalence relation $\sim$ on $\Sigma^*$.

Consider any trace closed language $L$ and the [[Monoids as Regular Languages|syntatic congruence]] $\equiv_L$.

> [!THM] Theorem 
> $\sim$ is finer than $\equiv_L$. That is, given any two words $u, v$ we have $u\sim v \Rightarrow u\equiv_L v$.

To show that, consider two trace-equivalent word $u, v$. For any words $x, y$ we have $x\cdot u\cdot y\sim x\cdot v\cdot y$.

But since $L$ is trace closed, for any trace congruent words $a, b$ we get $a\in L$ iff $b\in L$.

Therefore, give for any words $x, y$ if $x\cdot u\cdot y \in L$, we get that $x\cdot v\cdot y\in L$, thus $x\equiv_L y$.

> [!NOTE]
> Thus we can think of syntactic monoid of any automata that accepts a trace-closed language to instead accept traces. That is, we can think of the syntactic monoid as a map $(\Sigma ^* / \cong) \to M$, rather than $\Sigma^* \to M$.

---
# References
- [[Traces (Concurrency)]]
- [[Monoids as Regular Languages]]
- [[Monoids]]
