---
id: Synchronous Automata
aliases:
  - Synchronized Automata
tags:
  - Note
---
202601101945

Tags : [[Concurrency Theory]]
# Synchronous Automata
---
[[Direct Product Automata are not closed under boolean operations]]. This means that they are not always suitable for construction. Thus we close direct product languages under these boolean operations to get synchronized languages.

These are accepted by the following automata model which are called **synchronized automata**.

In a direct product automata, we have a set of accept states. That set of accept states can only be constructed as a product of states of the component automata, which makes it not closed under union, this we can allow all accept states that can be generated using products, and idea similar to [[Product topology]] and [[Product Measures]]. Since product of singleton final states is a singleton this can be phrased in a simpler form:

We allow any arbitrary collection of states of the product automata to be the set of final states.

Informally, we can consider a set of automata, one for each process, just like in [[Direct Product Automata]], but instead of having final states in each automata, we pick an arbitrary set of global states as our final states. The semantics are defined as follows:

> [!DEF] Definition
> A synchronized automata is defined using the following:
> - A distributed alphabet $\Sigma_\mathbb P$
> - A set of states $Q=\prod_{p\in \mathbb P} Q_p$
> - The set of start states is given by $Q_{\text {in}} = \prod_{p\in \mathbb P} Q_{\text {in}}^p$
> - let $(q_1,q_2,\dots,q_k), (q'_1,q'_2,\dots,q_k)\in Q$, then there is a transition $(q_1,q_2,\dots,q_k)\xrightarrow a (q'_1,q'_2,\dots,q'_k)$ if:
>   -  For each $j\in\text{loc}(a)$ we have $q_j\xrightarrow a q'_j$
>   -  For each $j\notin\text{loc}(a)$ we have $q_j=q_j'$ 
> - The set of final states $F\subseteq Q$

A language that can be recognized by a synchronized automata and not by a direct product automata is $\{a, b\}$ where the letters $a$ and $b$ are independent.

---
# References
- [[Product topology]]
- [[Product Measures]]
- [[Direct Product Automata are not closed under boolean operations]]
- [[Direct Product Automata]]
