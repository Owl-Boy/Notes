---
tags:
  - Note
aliases:
  - Degree of a Structure
---
202501302201

Tags : [[Finite Model Theory]]
# Degree of a Structure
---
There is a large class of structure which have a simple criteria for definability in [[First Order Logic|FO Logic]], that being that their [[Gaifman Graph]] having all vertices have a bounded degree.

We define the terms as follows
>[!definition] Degree
>Let $\sigma$ be a relational vocabulary, $R$ be an $m$-ary relation in $\sigma$ and $\mathfrak A \in \text{STRUCT}[\sigma]$. 
>For $a\in A$ and $i\leq m$, define $\text{degree}_{R, i}^\mathfrak A(a)$ as the cardinality of the set
>$$
>\{ (a_{1}\dots a_{i-1},a, a_{i+1}\dots a_{m})\in R^\mathfrak A\ |\ a_{1}\dots a_{i-1}, a_{i+1}\dots a_{m}\in A \}
>$$

This is the number of $m$ tuples, that have $a$ in the $i^\text{th}$ index and are in $R$.

>[!definition] Degree Set
>Let $\text{deg\_set}(\mathfrak A)$ to be the set of all numbers of the form $\text{degree}_{R, i}^\mathfrak A(a)$
>$$
>\text{deg\_set}(\mathfrak A) = \{ \text{degree}_{R, i}^\mathfrak A(a)\ |\ a\in A, R\in \sigma, i\leq \text{arity}(R)\}
>$$

It is the set of degrees that are realized in $\frak A$

>[!definition] Bounded Degree Structures
>$$
>\text{STRUCT}_{l}[\sigma] = \{ \mathfrak A \in \text{STRUCT}[\sigma]\ |\ \text{deg\_set}(\mathfrak A)\in \{ 1 \dots l \} \}
>$$

These are structures whose maximum degree is $l$.

We shall also be applying $\text{deg\_set}$ output of queries $\text{deg\_set}(Q(\mathfrak A))$ for any $m$-ary query $Q$, is the set of all degrees realized in the structure whose only $m$-ary relation is $Q$. 

---
# References
