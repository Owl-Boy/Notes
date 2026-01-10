---
id: Direct Product Automata are not closed under boolean operations
aliases:
  - Direct Product Automata are not closed under boolean operations
tags:
  - Note
  - Incomplete
---
202601101946

Tags : [[Concurrency Theory]]
# Direct Product Automata are not closed under boolean operations
---
[[Shuffle Closure|Shuffle closed]] languages are not closed under all boolean operations.

In the following sections, assume that the distributed alphabet is $\{\{a\}, \{b\}\}$

## Shuffle closed languages are NOT closed under union.

Consider the languages $\{a\}$ and $\{b\}$, their union is the language $\{a,b\}$, which is not shuffle closed, while the previous two languages are shuffle closed. The union should have accepted the empty string.

## Shuffle closed languages are NOT closed under complement.

Consider the shuffle closed language $\{\epsilon\}$. The complement of this language should contain all non-empty words, including $a$ and $b$, but if we take the shuffle closure of that language, we would have to add $\epsilon$, which is a contradiction.

## Shuffle closed languages ARE closed under intersection.

Consider 2 shuffle closed languages $A$ and $B$, and consider the intersection $A\cap B$. We need to show $C=\text{shuffle}(A\cap B)\subseteq A \cap B$.

Thus, consider any word $w\in C$, we get that for every process $p$, $w|_p\in A|_p$ and $w|_p\in B|_p$. Thus for any process $p$ $w|_p\in A$ and $w|_p \in B|_p$. This $w\in A\cap B$.

---
# References
- [[Shuffle Closure]]
- [[Distributed Alphabet]]
