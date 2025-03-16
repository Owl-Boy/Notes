---
tags:
  - Note
  - Incomplete
---
202503100903

Tags : [[Weighted Automata and Transducers]]
# Pure Sequential Transducer
---
A *Pure Sequential Transducer* is a weighted automata where the target semi-ring is also the set of words that can be constructed by some alphabet, so these work as functions from the set of words to another set of words and are defined as follows:

>[!definition]
>A **Pure Sequential Transducer** can be described by the following tuple:
>$$
>\langle Q, A, B, q_{0}, \delta, \phi \rangle
>$$
>where:
>- $A$ is the alphabet for the input
>- $B$ is the alphabet for the output
>- $Q$ is the set of states
>- $q_{0}$ is the initial state
>- $\delta$ is the transition function
>- $\phi$ assigns and output word in $B^*$ for some transitions (this is a partial function)

Pure Sequential transducers read letters one at a time producing outputs, they can be used to parse [[Prefix Codes]].

>[!todo] TODO: Add example

This is a special case of [[Sequential Transducers]].

---
# References
