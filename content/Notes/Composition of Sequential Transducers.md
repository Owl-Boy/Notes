---
tags:
  - Note
---
202503170303

Tags : [[Weighted Automata and Transducers]]
# Composition of Sequential Transducers
---
Given 2 sequential transducers
-  $f=(Q_{f}, A, B, q_{f}, m_{f}, \phi_{f}, \delta_{f},\rho_{f})$
-  $g=(Q_{g}, B, C, q_{g}, m_{g}, \phi_{g}, \delta_{g},\rho_{g})$
one construct the compostion of these 2 transducers defined as $g \circ f:A \to C$ as follows:
- $Q = Q_{f} \times Q_{g}$
- $q_{0}=(q_{f}, \delta(q_{g},m_{f}))$
	- When we start the computation, we notice that any word first passes through $f$, so any string that passes through $g$ will be after reading $m_{f}$ on $g$
- $m_{0} = m_{g}\cdot \phi(q_{g}, m_{f})$
	- All strings start with $m_{g}$ but the $g$ transducer also always reads $m_{f}$
- $\delta \equiv (p, q) \xrightarrow{a} (\delta_{f}(p, a), \delta(g, \phi(p, a)))$
	- This can be understood as, whenver we read a letter, we move normally in the $f$ transducer, but we take the output of $f$ and that is what is ready by $q$
- $\phi \equiv (p, q) \xrightarrow{a} \phi_{g} (\phi_{f}(a))$
	- This is easy, we read a letter in $f$ and then we pass the read word to $g$
- $\rho((p, q)) = \phi(q, \rho_{f}(p))\cdot \rho_{g}(\delta_{g}(q, \rho_{f}(p)))$
	- Here, we first read the ending letter of $f$, this is the first part of the string, then from the new state we read the ending string of $q$.

Together in a simple manner it looks like 
- $Q = Q_{f} \times Q_{g}$
- $q_{0}=(q_{f}, \delta(q_{g},m_{f}))$
- $m_{0} = m_{g}\cdot \phi(q_{g}, m_{f})$
- $\delta \equiv (p, q) \xrightarrow{a} (\delta_{f}(p, a), \delta(g, \phi(p, a)))$
- $\phi \equiv (p, q) \xrightarrow{a} \phi_{g} (\phi_{f}(a))$
- $\rho((p, q)) = \phi(q, \rho_{f}(p))\cdot \rho_{g}(\delta_{g}(q, \rho_{f}(p)))$
---
# References
