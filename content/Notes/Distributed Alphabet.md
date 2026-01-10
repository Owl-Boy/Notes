---
id: Distributed Automata
aliases:
  - Distributed Alphabet
tags:
  - Note
  - Incomplete
---
202601081303

Tags : [[Concurrency Theory]]
# Distributed Alphabet
---
Consider the following example of a run of a concurrent system:

> [!TODO] TODO: Add Example Diagram 

Let $\Sigma$ be the set of all letters used in the system.

> [!DEF] Definition 
> A *Distributed Alphabet* is the set of letters $\Sigma$ used by a distributed system, along with the information of what letters are recognized by which process, they are described by the following data:
> - Given:
>   - A set of process $\mathbb P$.
>   - A set of alphabets $\Sigma$
>   - For each process $p\in\mathbb P$, a set of letters $\Sigma_p\subseteq \Sigma$ recognized by it.
> - Distributed Language:
>   - The set $\Sigma_{\mathbb P}=\{ \Sigma_p \mid p\in \mathbb P \}$

There is also projection function $\pi_p:\Sigma^* \to \Sigma_p^*$ defined for each $p\in\mathbb P$ that drops the characters of the words not in $\Sigma_p$. 

Along with that, there is a function $\text{loc}:\Sigma\to 2^{\mathbb P}$ that takes a letter and gives the set of processes (locations) that recognize the letter.

---
# References
- [[Concurrency via Sharing Events]]
- [[Direct Product Automata]]
