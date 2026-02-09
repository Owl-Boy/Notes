---
id: Zielonka's Theorem
aliases:
  - Zielonka's Theorem
tags:
  - Note
  - Incomplete
---
202602092044

Tags : [[Concurrency Theory]]
# Zielonka's Theorem
---
> [!THM] Theorem 
> Let $L$ be a regular [[Traces (Concurrency)|trace]] language over a trace alphabet $\Sigma = (\hat\Sigma, \mathcal I)$. Then for every distributed alphabet $\Sigma_\mathbb P$ over the set of processes $\mathbb P$ such that the independence relation induced by $\Sigma_\mathbb P$ is $\mathcal I$, there is an [[Asynchronous Automata]] $\mathcal A$ over the alphabet $\Sigma_\mathbb P$ with $L(\mathcal A)=L$.

Given a regular language $L$ that is trace-closed, from [[Trace Independence is a Syntactic Congruence of Trace Languages]], we use the [[Construction of Syntactic Monoid of an Automata|Syntactic Monoid]] of the minimal DFA for the regular language, and will try to simulate that in a [[Gossip Automata]].
 
By [[Gossip Automata can be implemented as Asynchronous Automata]], we will be done.

Each process of the gossip automata tries to capture as much of the trace as its corresponding element of the syntactic monoid. But as it turns out, during a synchronization step, multiple of these functions would have to be combined in a non-trivial way, the problem is dealing with all of the shared information that is stored in the function. Thus it makes more sense for a process $p$ to not only store the function corresponding to its causal history, but for each subset $S\subseteq \mathbb P$ process $p$ should store what part of the trace it can see but $S$ cannot see. Thus during a synchronization step, we can simply compose the causal history for $S$ along with residue stored by $p$.

Note that causal history of any set of events is an ideal (say $I$), thus quotienting out by the ideal yeilds a residue $R$, and while thinking of linearization of the trace, we can assume that all events of $I$ happen before all events of $R$. Thus we can also assume that if $f_I$ and $f_R$ are the transitions corresponding to the traces in $A_{\text{DFA}}$ then the transition function corresponding the wholse set would be $f_I \triangleright f_R$. This shows that for the above automata, storing information of different parts of traces is fine as we are only dealing with ideals and residues.

---
# References

