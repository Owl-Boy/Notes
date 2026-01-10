---
id: Concurrency via Sharing Events
aliases:
  - Concurrency via Sharing Events
tags:
  - Note
---
202601081229

Tags : [[Concurrency Theory]]
# Concurrency via Sharing Events
---
Concurrency involves multiple processes running, either parallel-y or concurrently, for these processes to collectively solve a problem, they would have to communicate, and one way to do so is to have events, recognized by multiple automata.

An execution of such an event synchronizes the processes that recognize the event, which is used to coordinate processes together in order to solve the problem.

This study of this system starts with the following concepts:
- [[Distributed Alphabet]], for describing systems involving multiple processes, and 
- [[Traces (Concurrency)|Traces]] which capture an equivalence between different runs of the system that differ at parts that don't interact with each other.

---
# References
- [[Distributed Alphabet]]
- [[Traces (Concurrency)]]

