---
id: Distributed Alphabet
aliases:
  - Direct Product Automata
tags:
  - Note
---
202601081326

Tags : [[Concurrency Theory]]
# Direct Product Automata
---
An **direct product automata** is a collection of finite state automata, one for each process that together run on words of the alphabet $\Sigma$. 


> [!def] Definition
> Direct Product Automata are defined by a tuple containing the following components:
> - $\Sigma_{\mathbb P}$,  A distributed language 
> - An automata $A_p$ for each $p\in \mathbb P$ that runs over words of the alphabet $\Sigma_p$.

The semantics of this model are given by taking making a finite state automata, whose states represent the global configuration of the direct product automata. This can be constructed by the following construction.

The **direct product construction**, takes the distributed automata $A_\mathbb P$ and converts it to a finite state automata $|A_\mathbb P|$ in an attempt to capture its language (Also denoted as $\langle A_1 \| A_2 \| \dots \|A_k\rangle$ if $|\mathbb P|=k$).

The rough idea is to look at the configuration of the system in the run of a word. When a letter is read, all processes that recognize the letter take a step, while all other process don't move. Thus we break down our construction into the following step:
- To each automata $A_i$ on each state, add self loops for letters in $\Sigma \setminus \Sigma_i$.
  - This makes the language of all automata $\Sigma$, while preserving each projection of the language.
- Do a production construction and accept the intersection of all of the languages. 

More formally, the direct product automata $|A_\mathbb P|$ is defined as a tuple with the following components:
- $Q = Q_1 \times Q_2 \times \dots \times Q_k$
- let $(q_1,q_2,\dots,q_k), (q'_1,q'_2,\dots,q_k)\in Q$, then there is a transition $(q_1,q_2,\dots,q_k)\xrightarrow a (q'_1,q'_2,\dots,q'_k)$ if:
  -  For each $j\in\text{loc}(a)$ we have $q_j\xrightarrow a q'_j$
  -  For each $j\notin\text{loc}(a)$ we have $q_j=q_j'$ 
- $Q_{\text{in}} = Q_{\text{in}}^1\times Q_{\text{in}}^2\times\dots\times Q_{\text{in}}^k$  
- $F_{\text{in}} = F_{\text{in}}^1\times F_{\text{in}}^2\times\dots\times F_{\text{in}}^k$  

Note that only the languages that are fixed points of [[Shuffle Closure]] are accepted by this automata.

---
# References
- [[Distributed Alphabet]]
- [[Shuffle Closure]]
