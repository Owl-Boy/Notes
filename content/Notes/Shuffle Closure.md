---
id: Shuffle Closure
aliases:
  - Shuffle Closure
tags:
  - Note
---
202601081408

Tags : [[Concurrency Theory]]
# Shuffle Closure
---
Given a language $L$, over a distributed alphabet $\Sigma_\mathbb P$ is defined as the following set:
$$
\text{shuffle}(L, \Sigma_\mathbb P) = \{w : \Sigma^*\mid \forall p:\mathbb P, \exists u_p: L, w\downarrow_p=u\downarrow_p\} 
$$

> [!NOTE]
> For a language to be accepted by a [[Distributed Alphabet and Automata|distributed automata]], it needs to be a fixed point of the shuffle closure.

---
# References
- [[Distributed Alphabet and Automata]]
