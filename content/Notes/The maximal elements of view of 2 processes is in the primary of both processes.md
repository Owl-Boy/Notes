---
id: The maximal elements of view of 2 processes is in the primary of both processes
aliases:
  - The maximal elements of view of 2 processes is in the primary of both processes
tags:
  - Note
  - Incomplete
---
202601292355

Tags : [[Concurrency Theory]]
# The maximal elements of view of 2 processes is in the primary of both processes
---
Let $\partial_p$ be the sub-partial order of events that are causally related to events that recognize $p$.

Given processes $p$ and $q$. If $\max_p \le \max_q$ then $\partial_p = \partial_p\cap\partial_q$. Then $\max_q$ is in the primary of both the processes.

When $\max_p$ and $\max_q$ are incomparable. Let $e$ be a maximal element of $\partial_p\cap\partial_q$. Consider a path $p_1 : e\to\max_p$ and $p_2 : e\to\max_q$, none of the paths intersect, otherwise they would contradict the maximality of $e$. Let $r$ and $s$ be event right after $e$. Neither $r$, nor $s$ are local events, and we have that $r\in \partial_p\setminus\partial_q$ and $s\in\partial_q\setminus\partial_p$. Thus for process at which $r$ and $e$ coincide $e$ is the primary event for $q$ and the process where $s$ and $e$ coincide, $e$ is the primary event for $p$. Thus $e$ is in the primary of both processes. 

---
# References
- [[Gossip Problem]]
- [[Gossip Automata]]
- [[Gossip Automata can be implemented as Asynchronous Automata]]
