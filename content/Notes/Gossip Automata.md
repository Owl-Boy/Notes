---
id: Gossip Automata
aliases:
  - Gossip Automata
tags:
  - Note
---
202601292303

Tags : [[Concurrency Theory]]
# Gossip Automata
---
Gossip Automata is a modification of [[Asynchronous Automata]] such that each process carries information about about all other processes. 

To be more precise, given a process $p$, it remember the latest event $e_{p'}$ for every other $p$ which is in $p'$ view.

- This information is called the **primary graph**.
- Given any 2 processes $p$ and $p'$ whenever an event $e$ happens that is recognized by both processes (a synchronization events), both of them shared the information they have. Since the latest event on both processes is common, both process share the same causal history and hence now have the same gossip.
- Assuming there is an initial event shared by all events making all causal histories intersect. At any point of time, any pair of processes share some amount of gossip, this information is can be used to order events in gossip.

---
# References
- [[Gossip Problem]]
