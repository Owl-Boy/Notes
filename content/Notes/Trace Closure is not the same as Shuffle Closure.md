---
id: Trace Closure is not the same as Shuffle Closure
aliases:
  - Trace Closure is not the same as Shuffle Closure
tags:
  - Example
---

202601081507

tags : [[Concurrency Theory]]

#  Trace Closure is not the same as Shuffle Closure
---
While trace closure and shuffles closures are both operations that are meant to take a language and give the smallest, but bigger language accept by concurrent systems they are not the same.

Every shuffle closed language is trace-closed, but not every trace closed language is shuffle closed.

As a counter example, consider the alphabet $\Sigma = \{a, b\}$. We give the independence relation $\mathcal I = \{(a, b)\}$ and the distributed alphabet over 2 process $\Sigma_1 = {a}$ and \Sigma_2 = {b}$. Note that in both cases the letters $a$ and $b$ are independent. Now consider the language $L = \{a, b\} but we have:
- $\text{shuffle}(L) = \{a,b,ab,ba\}$ but 
- $\text{trace}(L) = \{a, b\}$

---
# Related
- [[Traces (Concurrency)|Trace]]
- [[Shuffle Closure]]
