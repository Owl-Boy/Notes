---
id: Gossip Automata can be implemented as Asynchronous Automata
aliases:
  - Gossip Automata can be implemented as Asynchronous Automata
tags:
  - Note
  - Incomplete
---
202601292349

Tags : [[Concurrency Theory]]
# Gossip Automata can be implemented as Asynchronous Automata
---
> [!LEM] Lemma 
> Given primary graphs of $p$ and $q$ before a synchronizing event, we can construct their primary graphs after the synchronizing event.

Let $r$ be a process, let $e_{p}$ and $e_{q}$ be the primary events of $r$ from the perspective of $p$ and $q$ respectively.

If $e_p\le e_q$ then $e_p\in \partial_p\cap\partial_q$ and hence is dominated by a maximal event of $\partial_p\cap\partial_q$ which is in the primary graphs of both $p$ and $q$.

> [!THM] 
> A Gossip Automata can be implemented as an Asynchronous Automata.

The previous construction goes through if each event can be labelled uniquely. From the previous lemma, we only need to take care of the events that are in the primary of each of the process. This given a process $p$, we only need to uniquely label the events that are in the $p$-primary for all process.

Given any other process $q$, let $e$ be an event in the primary for process $p$. Consider an imaginary synchronization event of process $p$ and $q$, we can use the previous lemma to show that there is an element in the primary of both $p$ and $q$ that dominates $e$. Due to this, we count $e$ in the secondary information of $p$ primary of a primary process.

The secondary information can be captured in an $n\times n$ table. While the primary graph is an $n$ graph. Thus, the total number of combinations is $|\Sigma|^{n^2} \times (|\Sigma|^n\times 2^{n^2})$, which is $2^{O(n^2\log|\Sigma|)}$

This each process has at most $2^{O(n^2\log|\Sigma|)}$ blow up in the number of states.

---
# References
- [[Gossip Automata]] 
- [[Asynchronous Automata]]
- [[The maximal elements of view of 2 processes is in the primary of both processes]]
