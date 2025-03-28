---
tags:
  - Note
---
202503170303

Tags : [[Weighted Automata and Transducers]]
# Pre-Image of a Regular Language under a Sequential Transducer is Regular
---
>[!theorem]
>Consider a regular language $L \subseteq B^*$ and a [[Sequential Transducers]] $f: A^* \to B^*$, then the language $L'=f^{-1}(L) \subseteq A^*$ is regular.

Let $L$ be a regular language and $\mathcal{A}=(Q_{\mathcal{A}}, q_{(0, \mathcal{A})}, F_{\mathcal{A}}, \delta_{\mathcal{A}})$ be a deterministic automaton for this and let $f=(Q_{f}, A, B, q_{(0, f)}, m_{0}, \phi, \delta_{f},\rho)$ be a sequential transducer. We now construct an automata for $f^{-1}(L)$ in the following way:
- $Q = Q_{\mathcal{A}}\times Q_{f}$
- $q_{0} = (\delta_{\mathcal{A}}(q_{(0, \mathcal{A})}, m_{0}), q_{(0, f)})$
	- This denotes that we read the string $m_{0}$ in $\mathcal{A}$ always first.
- $F = \{ (q, p) \mid \delta(q, \rho (p)) \in F_{\mathcal{A}} \}$
- for each $a \in A$ we have $(q, p) \to (\delta_{\mathcal{A}}(q, \phi(p, a), \delta_{f}(p, a))$

This describes a non-deterministic automata whose language is $f^{-1}(L)$

---
# References
