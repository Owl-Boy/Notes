---
tags:
  - Note
  - Incomplete
---
202504150504

Tags : [[Finite Model Theory]]
# Immerman–Vardi's Theorem
---
>[!theorem]
>[[Fixed Point Logics|LFP]] [[Logic L capturing the complexity class K|captures]] [[P (Complexity Class)|PTime]] over the class of ordered structures.
>
>$$
>\text{LFP} + <\quad = \quad \text{Ptime}
>$$

To show that the data complexity of $\text{LFP}+<$ is in $\text{P}$, we induct on the size of the formula, most of it is discussed in [[Complexity of FO]]. Except for the computation of the fixed point.

For this we only need to show that one step of the operator works in polytime, as the operator is run $|U|$ times where $U$ is the universe. This is also true because one execution of the operator is evaluating a function known to be in $P$, $|U|$ times, starting with an $\text{FO}$ formula in the base case.

For the other direction, the proof is similar to [[Trakhtenbrot's Theorem]] and [[Fagin's Theorem]] where we construct a formula for a deterministic [[Turing Machines|Turing machine]] that holds iff the turing machine accepts the input in polynomial time.

---
# References
