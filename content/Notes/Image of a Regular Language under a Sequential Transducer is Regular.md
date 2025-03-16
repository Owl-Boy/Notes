---
tags:
  - Note
---
202503170203

Tags : [[Weighted Automata and Transducers]]
# Image of a Regular Language under a Sequential Transducer is Regular
---
>[!theorem]
>Consider a regular language $L \subseteq A^*$ and a [[Sequential Tranducers]] $f : A^* \to B^*$, then the language which is the image $L' = f(L) \subseteq B^*$.

Let $L$ be a regular language and $\mathcal{A}=(Q_{\mathcal{A}}, q_{0}, F_{\mathcal{A}}, \delta_{\mathcal{A}})$ be a deterministic automaton for this and let $f=(Q_{f}, A, B, q_{0}, m_{0}, \phi, \delta_{f},\rho)$ be a sequential transducer. We now construct an automata for $f(L)$ in the following way:
- $Q = Q_{\mathcal{A}} \times Q_{f} \sqcup \{ q_{\text{start}}, q_{\text{fin}} \}$
- $q_{0} = q_{\text{start}}$
- $F = \{ q_{\text{fin}} \}$
- The transition function is a bit more complicated and will be described in steps:
	- Given a state $(q, p)$ if we were to read an alphabet $a$, that would change states in the input automata and transducer, and our new automata gets to read the the output of the transition. 
		- For each $a\in A, (q, p) \xrightarrow{\phi(p, a)}(\delta_{\mathcal{A}}(q, a), \delta_{f}(p, a))$
	- All string must start with $m_{0}$ and only then can the above computation can begin
		- $q_{start} \xrightarrow{m_{0}}(q_{(0, \mathcal{A})}, q_{(0, f)})$
	- All words endings are decided by $\rho$ in the transducer and hence we have
		- $(\_{, p})\xrightarrow{\rho(p)} q_{\text{fin}}$

This describes a non-deterministic automata who language is the image of $L$ under $f$, so we are done.

---
# References
