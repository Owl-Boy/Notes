---
tags:
  - Note
---
202503170303

Tags : [[Weighted Automata and Transducers]]
# A Language if Regular iff its Characteristic Function is regular
---
>[!theorem]
>Let $L$ be a language and $\chi_{L}$ be its characteristic function, we have that $L$ is regular iff $\chi_{L}$ is regular.

If a language is regular, it is easy to construct its characterisitic function, we define $m_{0}=\epsilon$ and output for every transition to be $\epsilon$. For definition $\rho$ we say $\rho(q)=1$ if $q$ is a final state for the regular automata for the language $0$ otherwise.

For the other direction, note that a characteristic function is a total function from $\Sigma^* \to \{ 0, 1 \}$ so we can make the following cases:
- if $m_{0} = 1$ then the language is $\Sigma^*$
- if $m_{0} = 0$ then the language is empty
- For any state $q$ If $\rho(q)=1$ then we mark it as a final state
- We also add an extra reject and accept state such that all transition that create $1$ are now redirected to the new accept state where it loops, and all transitions that create a $0$ are redirected to the reject state and they loop there

---
# References
