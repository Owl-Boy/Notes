---
tags:
  - Note
---
202503202203

Tags : [[Weighted Automata and Transducers]]
# Computing $m_{q}$
---
In the construction of [[Normalizing a Transducer]]. An important step was to figure out, given a state what is the longest common prefix of every word that can be read from it.

To compute that, one can simply start branching over all paths to compute this until a distinguishing suffix is found or a word ends. In doing so while branching one also computes this for other states.

---
# References
